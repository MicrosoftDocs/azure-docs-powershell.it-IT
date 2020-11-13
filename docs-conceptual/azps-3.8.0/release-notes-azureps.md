---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 966b6ef2fe8e0a52cf230520015e1a92cd29fe1a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410180"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="39f18-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="39f18-103">Azure PowerShell release notes</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="39f18-104">3.8.0 - Aprile 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-104">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="39f18-105">Novità rispetto all'ultima versione</span><span class="sxs-lookup"><span data-stu-id="39f18-105">Highlights since the last release</span></span>
* <span data-ttu-id="39f18-106">Versioni di PowerShell supportate da Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4 e versioni successive, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="39f18-106">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-107">Az.Accounts</span></span>
* <span data-ttu-id="39f18-108">Aggiornamento dell'URL del sondaggio di Azure PowerShell in 'Resolve-AzError' [#11507]</span><span class="sxs-lookup"><span data-stu-id="39f18-108">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39f18-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-109">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-110">Aggiunta di un avviso di modifica di rilievo per la modifica dell'output dei cmdlet di File di Azure in una versione futura</span><span class="sxs-lookup"><span data-stu-id="39f18-110">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="39f18-111">Aggiornamento della documentazione di 'Set-AzApiManagementGroup' per specificare il parametro GroupId</span><span class="sxs-lookup"><span data-stu-id="39f18-111">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-112">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-112">Az.Cdn</span></span>
* <span data-ttu-id="39f18-113">Correzione della visualizzazione dello SKU con prezzi relativi a ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="39f18-113">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-114">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-114">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-115">Supporto di Identity, Encryption, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="39f18-115">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-116">Az.Compute</span></span>
* <span data-ttu-id="39f18-117">Aggiunta del cmdlet 'Set-AzVmssOrchestrationServiceState'.</span><span class="sxs-lookup"><span data-stu-id="39f18-117">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="39f18-118">'Get-AzVmss' con -InstanceView visualizza gli stati OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="39f18-118">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-119">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-119">Az.IotHub</span></span>
* <span data-ttu-id="39f18-120">Gestione della configurazione dei dispositivi gemelli IoT. I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-120">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="39f18-121">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="39f18-121">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="39f18-122">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="39f18-122">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="39f18-123">Aggiunta del cmdlet per richiamare il metodo diretto in un dispositivo di un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-123">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="39f18-124">Gestione della configurazione dei dispositivi gemelli del modulo per i dispositivi. I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-124">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="39f18-125">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="39f18-125">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="39f18-126">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="39f18-126">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="39f18-127">Gestione della configurazione della gestione automatica dei dispositivi IoT su larga scala.</span><span class="sxs-lookup"><span data-stu-id="39f18-127">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="39f18-128">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-128">New cmdlets are:</span></span>
    - <span data-ttu-id="39f18-129">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="39f18-129">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="39f18-130">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="39f18-130">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="39f18-131">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="39f18-131">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="39f18-132">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="39f18-132">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="39f18-133">Aggiunta del cmdlet per richiamare un metodo del modulo Edge in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-133">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-134">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-135">Aggiunta di un nuovo cmdlet 'Update-AzKeyVault' che può abilitare l'eliminazione temporanea e la protezione da eliminazione in un insieme di credenziali</span><span class="sxs-lookup"><span data-stu-id="39f18-135">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="39f18-136">Aggiunta del supporto a Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="39f18-136">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="39f18-137">Correzione dell'errore negli esempi di 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="39f18-137">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="39f18-138">Aggiunta del supporto per l'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="39f18-138">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="39f18-139">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="39f18-139">Az.Maintenance</span></span>
* <span data-ttu-id="39f18-140">Pubblicazione della versione finale dei cmdlet di manutenzione per la disponibilità generale</span><span class="sxs-lookup"><span data-stu-id="39f18-140">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-141">Az.Monitor</span></span>
* <span data-ttu-id="39f18-142">Aggiunta di cmdlet per l'ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="39f18-142">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="39f18-143">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="39f18-143">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="39f18-144">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="39f18-144">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="39f18-145">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="39f18-145">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="39f18-146">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="39f18-146">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="39f18-147">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="39f18-147">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="39f18-148">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="39f18-148">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="39f18-149">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="39f18-149">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-150">Az.Network</span></span>
* <span data-ttu-id="39f18-151">Aggiornamento dei cmdlet per abilitare la connessione su IP privato per il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39f18-151">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="39f18-152">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="39f18-152">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="39f18-153">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="39f18-153">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="39f18-154">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="39f18-154">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="39f18-155">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="39f18-155">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="39f18-156">Aggiornamento dei cmdlet per abilitare LocalNetworkGateways e VpnSites basati su FQDN</span><span class="sxs-lookup"><span data-stu-id="39f18-156">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="39f18-157">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="39f18-157">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="39f18-158">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="39f18-158">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="39f18-159">Aggiunta del supporto per la famiglia di indirizzi IPv6 in ExpressRouteCircuitConnectionConfig (Copertura globale)</span><span class="sxs-lookup"><span data-stu-id="39f18-159">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="39f18-160">Aggiunta di 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="39f18-160">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="39f18-161">Consente di impostare tutte le proprietà esistenti, tra cui IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="39f18-161">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="39f18-162">Aggiornamento di 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="39f18-162">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="39f18-163">Aggiunta di un altro parametro facoltativo AddressPrefixType per specificare la famiglia di indirizzi del prefisso di indirizzi</span><span class="sxs-lookup"><span data-stu-id="39f18-163">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="39f18-164">Aggiornamento dei cmdlet per consentire l'impostazione del timeout DPD nelle connessioni del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39f18-164">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="39f18-165">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-165">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="39f18-166">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-166">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-167">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-167">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-168">Aggiunta del cmdlet 'Start-AzPolicyComplianceScan' per attivare le analisi di conformità ai criteri</span><span class="sxs-lookup"><span data-stu-id="39f18-168">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="39f18-169">Aggiunta di definizione dei criteri, definizione di set e versioni di assegnazione all'output di 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="39f18-169">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-170">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-170">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-171">Miglioramento della formattazione del codice e dell'usabilità degli esempi di 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="39f18-171">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-172">Az.Sql</span></span>
* <span data-ttu-id="39f18-173">Aggiunta dei cmdlet 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation'</span><span class="sxs-lookup"><span data-stu-id="39f18-173">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="39f18-174">Supporto del controllo di un account di archiviazione nella rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39f18-174">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-175">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-175">Az.Storage</span></span>
* <span data-ttu-id="39f18-176">Aggiunta di un avviso di modifica di rilievo per la modifica dell'output dei cmdlet di File di Azure in una versione futura</span><span class="sxs-lookup"><span data-stu-id="39f18-176">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="39f18-177">Supporto dei nuovi elementi SkuName StandardGZRS, StandardRAGZRS per la creazione e l'aggiornamento di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="39f18-177">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="39f18-178">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39f18-178">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="39f18-179">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39f18-179">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="39f18-180">Supporto di DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="39f18-180">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="39f18-181">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="39f18-181">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="39f18-182">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="39f18-182">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="39f18-183">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="39f18-183">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="39f18-184">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="39f18-184">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="39f18-185">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="39f18-185">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="39f18-186">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="39f18-186">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="39f18-187">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="39f18-187">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="39f18-188">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="39f18-188">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="39f18-189">0.10.0-preview - Aprile 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-189">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="39f18-190">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-190">General</span></span>
* <span data-ttu-id="39f18-191">Disponibilità di moduli Az in anteprima nell'hub di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="39f18-191">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="39f18-192">Consentono la compatibilità multipiattaforma con Linux e macOS.</span><span class="sxs-lookup"><span data-stu-id="39f18-192">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="39f18-193">L'hub di Azure Stack ora supporta PowerShell core con i moduli Az. Per altre informazioni, vedere [qui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="39f18-193">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="39f18-194">I moduli Az supportano il profilo 2019-03-01-ibrido:</span><span class="sxs-lookup"><span data-stu-id="39f18-194">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="39f18-195">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="39f18-195">Az.Billing</span></span>
  - <span data-ttu-id="39f18-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-196">Az.Compute</span></span>
  - <span data-ttu-id="39f18-197">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="39f18-197">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="39f18-198">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-198">Az.EventHub</span></span>
  - <span data-ttu-id="39f18-199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-199">Az.IotHub</span></span>
  - <span data-ttu-id="39f18-200">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-200">Az.KeyVault</span></span>
  - <span data-ttu-id="39f18-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-201">Az.Monitor</span></span>
  - <span data-ttu-id="39f18-202">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-202">Az.Network</span></span>
  - <span data-ttu-id="39f18-203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-203">Az.Resources</span></span>
  - <span data-ttu-id="39f18-204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-204">Az.Storage</span></span>
  - <span data-ttu-id="39f18-205">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-205">Az.Websites</span></span>
* <span data-ttu-id="39f18-206">Sono stati introdotti tre nuovi moduli di PowerShell per az compatibili con l'hub di Azure Stack, ovvero Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-206">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="39f18-207">I comandi rimangono relativamente invariati, con modifiche minime come la sostituzione di AzureRM con Az</span><span class="sxs-lookup"><span data-stu-id="39f18-207">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="39f18-208">Il collegamento aggiornato alla documentazione di PowerShell per l'hub di Azure Stack è reperibile [qui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="39f18-208">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="39f18-209">3.7.0 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-209">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-210">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-210">Az.Accounts</span></span>
* <span data-ttu-id="39f18-211">Correzione dell'eccezione NullReferenceException generata da 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' in caso di mancato accesso [#10292]</span><span class="sxs-lookup"><span data-stu-id="39f18-211">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-212">Az.Compute</span></span>
* <span data-ttu-id="39f18-213">Aggiunta dei parametri seguenti al cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="39f18-213">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="39f18-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="39f18-214">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="39f18-215">Proprietà Encryption consentita per il parametro Target del cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="39f18-215">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="39f18-216">Correzione del problema tempDisk per i cmdlet 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="39f18-216">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="39f18-217">[#11354]</span><span class="sxs-lookup"><span data-stu-id="39f18-217">[#11354]</span></span>
* <span data-ttu-id="39f18-218">Aggiunta del supporto dei cmdlet seguenti per la nuova estensione SAP</span><span class="sxs-lookup"><span data-stu-id="39f18-218">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="39f18-219">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39f18-219">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="39f18-220">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39f18-220">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="39f18-221">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39f18-221">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="39f18-222">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="39f18-222">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="39f18-223">Correzione di errori negli esempi del documento della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-223">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="39f18-224">Visualizzazione del valore stringa esatto per PowerState VM nel formato tabella.</span><span class="sxs-lookup"><span data-stu-id="39f18-224">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="39f18-225">'New-AzVmssConfig': correzione della serializzazione della proprietà AutomaticRepairs quando SinglePlacementGroup è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="39f18-225">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="39f18-226">[#11257]</span><span class="sxs-lookup"><span data-stu-id="39f18-226">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-227">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-228">Aggiornamento di ADF .NET SDK alla versione 4.8.0</span><span class="sxs-lookup"><span data-stu-id="39f18-228">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="39f18-229">Aggiunta di parametri facoltativi al comando 'Invoke-AzDataFactoryV2Pipeline' per supportare la riesecuzione</span><span class="sxs-lookup"><span data-stu-id="39f18-229">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-230">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-230">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-231">Aggiunta della descrizione della modifica di rilievo per 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="39f18-231">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="39f18-232">Aggiunta dell'opzione di codifica Byte per 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="39f18-232">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39f18-233">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-233">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-234">Supporto della versione minima supportata di TLS durante la creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="39f18-234">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-235">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-235">Az.IotHub</span></span>
* <span data-ttu-id="39f18-236">Aggiunta del supporto per gestire le impostazioni distribuite per singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39f18-236">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="39f18-237">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-237">New Cmdlets are:</span></span>
    - <span data-ttu-id="39f18-238">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="39f18-238">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="39f18-239">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="39f18-239">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-240">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-240">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-241">Aggiunta degli attributi della modifica di rilievo a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="39f18-241">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-242">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-242">Az.Monitor</span></span>
* <span data-ttu-id="39f18-243">Documentazione aggiornata per 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="39f18-243">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-244">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-244">Az.Network</span></span>
* <span data-ttu-id="39f18-245">Aggiornamento dei cmdlet per consentire VirtualHubVnetConnections tra tenant</span><span class="sxs-lookup"><span data-stu-id="39f18-245">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="39f18-246">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="39f18-246">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="39f18-247">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="39f18-247">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="39f18-248">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="39f18-248">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="39f18-249">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="39f18-249">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="39f18-250">Rimozione della dipendenza di SQL Management SDK</span><span class="sxs-lookup"><span data-stu-id="39f18-250">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-251">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-251">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-252">Miglioramento dei messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="39f18-252">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-254">Azure Site Recovery: aggiunto il supporto per la riprotezione e aggiornamento delle proprietà delle VM per le macchine virtuali con crittografia dischi di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-254">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="39f18-255">Azure Site Recovery: aggiunta del monitoraggio per il ripristino di emergenza nelle proprietà VmwareToAzure</span><span class="sxs-lookup"><span data-stu-id="39f18-255">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="39f18-256">Backup di Azure: aggiunta del supporto per la ripetizione dell'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="39f18-256">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="39f18-257">Backup di Azure: aggiunta del supporto per le impostazioni di esclusione disco durante il backup e il ripristino.</span><span class="sxs-lookup"><span data-stu-id="39f18-257">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="39f18-258">Backup di Azure: aggiunta del supporto per il ripristino di più file/cartelle in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="39f18-258">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="39f18-259">Backup di Azure: aggiunta del supporto per il gruppo di risorse specificato dall'utente durante l'aggiornamento dei criteri IaasVM</span><span class="sxs-lookup"><span data-stu-id="39f18-259">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-260">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-260">Az.Resources</span></span>
* <span data-ttu-id="39f18-261">Correzione di 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' per l'utilizzo del valore effettivo di apiVersion per le risorse invece di quello predefinito [#11267]</span><span class="sxs-lookup"><span data-stu-id="39f18-261">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="39f18-262">Aggiunta della registrazione di correlationId per gli scenari di errore</span><span class="sxs-lookup"><span data-stu-id="39f18-262">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="39f18-263">Modifica di lieve entità alla documentazione di 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="39f18-263">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="39f18-264">Aggiunta dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="39f18-264">Added example.</span></span>
* <span data-ttu-id="39f18-265">Aggiunta della virgoletta singola come carattere di escape nel valore di parametro 'Get-AzADUser' [#11317]</span><span class="sxs-lookup"><span data-stu-id="39f18-265">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="39f18-266">Aggiunta di nuovi cmdlet per gli script di distribuzione ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="39f18-266">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-267">Az.Sql</span></span>
* <span data-ttu-id="39f18-268">Aggiunta del parametro secondario leggibile a 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="39f18-268">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="39f18-269">Aggiunta del cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="39f18-269">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="39f18-270">Salvataggio della classificazione di riservatezza durante la classificazione delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="39f18-270">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="39f18-271">Az.Support</span><span class="sxs-lookup"><span data-stu-id="39f18-271">Az.Support</span></span>
* <span data-ttu-id="39f18-272">Disponibilità generale del modulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="39f18-272">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-273">Az.Websites</span></span>
* <span data-ttu-id="39f18-274">Aggiunta del supporto per l'uso delle regole di gestione del traffico delle app Web con i nuovi cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="39f18-274">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="39f18-275">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39f18-275">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="39f18-276">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39f18-276">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="39f18-277">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39f18-277">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="39f18-278">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="39f18-278">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="39f18-279">3.6.1 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-279">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-280">Az.Accounts</span></span>
* <span data-ttu-id="39f18-281">Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]</span><span class="sxs-lookup"><span data-stu-id="39f18-281">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="39f18-282">Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]</span><span class="sxs-lookup"><span data-stu-id="39f18-282">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="39f18-283">Aggiunta la versione Az in UserAgent</span><span class="sxs-lookup"><span data-stu-id="39f18-283">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39f18-284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-284">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-285">Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="39f18-285">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="39f18-286">'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="39f18-286">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="39f18-287">'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON</span><span class="sxs-lookup"><span data-stu-id="39f18-287">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="39f18-288">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="39f18-288">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-289">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-289">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-290">Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="39f18-290">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-291">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-291">Az.IotHub</span></span>
* <span data-ttu-id="39f18-292">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-292">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="39f18-293">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-293">New Cmdlets are:</span></span>
    - <span data-ttu-id="39f18-294">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-294">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39f18-295">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-295">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39f18-296">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-296">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39f18-297">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-297">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="39f18-298">Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-298">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="39f18-299">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-299">New Cmdlets are:</span></span>
    - <span data-ttu-id="39f18-300">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39f18-300">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="39f18-301">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39f18-301">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="39f18-302">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39f18-302">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="39f18-303">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="39f18-303">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="39f18-304">Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-304">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="39f18-305">Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-305">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="39f18-306">Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-306">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="39f18-307">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-307">New Cmdlets are:</span></span>
    - <span data-ttu-id="39f18-308">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="39f18-308">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="39f18-309">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="39f18-309">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="39f18-310">Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39f18-310">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-311">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-311">Az.Monitor</span></span>
* <span data-ttu-id="39f18-312">Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]</span><span class="sxs-lookup"><span data-stu-id="39f18-312">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-313">Az.Network</span></span>
* <span data-ttu-id="39f18-314">Aggiornamento di SQL Management SDK.</span><span class="sxs-lookup"><span data-stu-id="39f18-314">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="39f18-315">Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="39f18-315">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="39f18-316">Mapping del campo ActionsRequired a ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="39f18-316">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="39f18-317">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="39f18-317">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-318">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-318">Az.Resources</span></span>
* <span data-ttu-id="39f18-319">Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="39f18-319">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="39f18-320">Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]</span><span class="sxs-lookup"><span data-stu-id="39f18-320">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="39f18-321">Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]</span><span class="sxs-lookup"><span data-stu-id="39f18-321">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="39f18-322">Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]</span><span class="sxs-lookup"><span data-stu-id="39f18-322">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="39f18-323">Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="39f18-323">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="39f18-324">Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri</span><span class="sxs-lookup"><span data-stu-id="39f18-324">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="39f18-325">Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server</span><span class="sxs-lookup"><span data-stu-id="39f18-325">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="39f18-326">Estensione dei cmdlet Tag per l'accettazione di -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f18-326">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="39f18-327">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f18-327">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="39f18-328">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f18-328">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="39f18-329">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f18-329">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="39f18-330">Aggiunta di nuovi cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="39f18-330">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="39f18-331">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="39f18-331">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="39f18-332">Inclusione di ScopedDeployment da SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="39f18-332">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-333">Az.Sql</span></span>
* <span data-ttu-id="39f18-334">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="39f18-334">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="39f18-335">Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti</span><span class="sxs-lookup"><span data-stu-id="39f18-335">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="39f18-336">Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito</span><span class="sxs-lookup"><span data-stu-id="39f18-336">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="39f18-337">Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione</span><span class="sxs-lookup"><span data-stu-id="39f18-337">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="39f18-338">Rimozione di un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="39f18-338">Remove an LTR backup</span></span>
    - <span data-ttu-id="39f18-339">Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito</span><span class="sxs-lookup"><span data-stu-id="39f18-339">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="39f18-340">Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="39f18-340">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="39f18-341">Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-341">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="39f18-342">Bump della versione di SQL SDK per Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-342">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-343">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-343">Az.Storage</span></span>
* <span data-ttu-id="39f18-344">Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-344">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="39f18-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="39f18-345">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="39f18-346">Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura</span><span class="sxs-lookup"><span data-stu-id="39f18-346">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="39f18-347">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="39f18-347">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="39f18-348">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="39f18-348">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-349">Az.Websites</span></span>
* <span data-ttu-id="39f18-350">Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="39f18-350">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="39f18-351">Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web</span><span class="sxs-lookup"><span data-stu-id="39f18-351">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="39f18-352">Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="39f18-352">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="39f18-353">Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi</span><span class="sxs-lookup"><span data-stu-id="39f18-353">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="39f18-354">Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="39f18-354">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="39f18-355">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-355">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39f18-356">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="39f18-356">Highlights since the last major release</span></span>
* <span data-ttu-id="39f18-357">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="39f18-357">Updated client side telemetry.</span></span>
* <span data-ttu-id="39f18-358">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="39f18-358">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="39f18-359">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="39f18-359">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-360">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-360">Az.Accounts</span></span>
* <span data-ttu-id="39f18-361">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="39f18-361">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-362">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-362">Az.Automation</span></span>
* <span data-ttu-id="39f18-363">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="39f18-363">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-364">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-364">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-365">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="39f18-365">Updated SDK to 7.0</span></span>
* <span data-ttu-id="39f18-366">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="39f18-366">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-367">Az.Compute</span></span>
* <span data-ttu-id="39f18-368">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="39f18-368">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39f18-369">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-369">Az.FrontDoor</span></span>
* <span data-ttu-id="39f18-370">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="39f18-370">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-371">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-371">Az.IotHub</span></span>
* <span data-ttu-id="39f18-372">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-372">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="39f18-373">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-373">New Cmdlets are:</span></span>
    - <span data-ttu-id="39f18-374">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-374">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39f18-375">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-375">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39f18-376">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-376">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="39f18-377">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="39f18-377">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-378">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-379">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="39f18-379">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-380">Az.Monitor</span></span>
* <span data-ttu-id="39f18-381">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="39f18-381">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="39f18-382">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="39f18-382">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="39f18-383">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="39f18-383">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-384">Az.Network</span></span>
* <span data-ttu-id="39f18-385">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="39f18-385">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="39f18-386">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="39f18-386">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="39f18-387">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="39f18-387">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="39f18-388">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-388">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="39f18-389">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="39f18-389">No new cmdlets are added.</span></span> <span data-ttu-id="39f18-390">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-390">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-392">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="39f18-392">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-393">Az.Resources</span></span>
* <span data-ttu-id="39f18-394">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="39f18-394">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="39f18-395">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39f18-395">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="39f18-396">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="39f18-396">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="39f18-397">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="39f18-397">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="39f18-398">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="39f18-398">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="39f18-399">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="39f18-399">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="39f18-400">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="39f18-400">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="39f18-401">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-401">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-402">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-402">Az.Sql</span></span>
* <span data-ttu-id="39f18-403">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="39f18-403">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="39f18-404">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="39f18-404">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="39f18-405">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="39f18-405">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="39f18-406">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39f18-406">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="39f18-407">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="39f18-407">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39f18-408">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39f18-408">Az.StorageSync</span></span>
* <span data-ttu-id="39f18-409">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="39f18-409">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="39f18-410">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-410">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39f18-411">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="39f18-411">Highlights since the last major release</span></span>
* <span data-ttu-id="39f18-412">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="39f18-412">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="39f18-413">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="39f18-413">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-414">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-414">Az.Accounts</span></span>
* <span data-ttu-id="39f18-415">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="39f18-415">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="39f18-416">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="39f18-416">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39f18-417">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-417">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-418">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="39f18-418">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="39f18-419">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="39f18-419">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="39f18-420">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="39f18-420">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="39f18-421">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-421">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-422">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-422">Az.Compute</span></span>
* <span data-ttu-id="39f18-423">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="39f18-423">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="39f18-424">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="39f18-424">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="39f18-425">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="39f18-425">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="39f18-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-426">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="39f18-427">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="39f18-427">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-428">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-428">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-429">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="39f18-429">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="39f18-430">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="39f18-430">Az.DeploymentManager</span></span>
* <span data-ttu-id="39f18-431">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="39f18-431">Adds LIST operations for resources</span></span>
* <span data-ttu-id="39f18-432">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="39f18-432">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39f18-433">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-433">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-434">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="39f18-434">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-435">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-435">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-436">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="39f18-436">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-437">Az.Network</span></span>
* <span data-ttu-id="39f18-438">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="39f18-438">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="39f18-439">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="39f18-439">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="39f18-440">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="39f18-440">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="39f18-441">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="39f18-441">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="39f18-442">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="39f18-442">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="39f18-443">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="39f18-443">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="39f18-444">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="39f18-444">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="39f18-445">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="39f18-445">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="39f18-446">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-446">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-447">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="39f18-448">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-448">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="39f18-449">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="39f18-449">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="39f18-450">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="39f18-450">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-451">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-451">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-452">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="39f18-452">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="39f18-453">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="39f18-453">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="39f18-454">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="39f18-454">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="39f18-455">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="39f18-455">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-456">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-456">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-457">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="39f18-457">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="39f18-458">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="39f18-458">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-459">Az.Resources</span></span>
* <span data-ttu-id="39f18-460">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="39f18-460">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="39f18-461">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="39f18-461">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-462">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-462">Az.Sql</span></span>
<span data-ttu-id="39f18-463">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="39f18-463">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-464">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-464">Az.Storage</span></span>
* <span data-ttu-id="39f18-465">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="39f18-465">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="39f18-466">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-466">New-AzStorageAccount</span></span>
* <span data-ttu-id="39f18-467">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="39f18-467">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="39f18-468">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39f18-468">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-469">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-469">Az.Websites</span></span>
* <span data-ttu-id="39f18-470">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="39f18-470">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="39f18-471">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="39f18-471">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="39f18-472">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="39f18-472">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-473">Az.Accounts</span></span>
* <span data-ttu-id="39f18-474">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="39f18-474">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-475">Az.Cdn</span></span>
* <span data-ttu-id="39f18-476">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f18-476">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-477">Az.Compute</span></span>
* <span data-ttu-id="39f18-478">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="39f18-478">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="39f18-479">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-479">Az.ContainerInstance</span></span>
* <span data-ttu-id="39f18-480">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-480">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="39f18-481">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="39f18-481">Az.DataBoxEdge</span></span>
* <span data-ttu-id="39f18-482">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39f18-482">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39f18-483">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-483">Get the Edge Storage Container</span></span>
* <span data-ttu-id="39f18-484">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39f18-484">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39f18-485">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-485">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="39f18-486">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39f18-486">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39f18-487">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-487">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="39f18-488">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="39f18-488">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="39f18-489">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-489">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="39f18-490">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39f18-490">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="39f18-491">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-491">Get the Edge Storage Account</span></span>
* <span data-ttu-id="39f18-492">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39f18-492">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="39f18-493">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-493">Create new Edge Storage Account</span></span>
* <span data-ttu-id="39f18-494">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="39f18-494">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="39f18-495">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="39f18-495">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="39f18-496">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="39f18-496">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="39f18-497">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="39f18-497">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="39f18-498">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="39f18-498">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="39f18-499">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="39f18-499">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-500">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-501">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="39f18-501">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="39f18-502">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="39f18-502">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="39f18-503">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="39f18-503">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="39f18-504">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="39f18-504">Az.DevTestLabs</span></span>
* <span data-ttu-id="39f18-505">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="39f18-505">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-506">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-506">Az.EventHub</span></span>
* <span data-ttu-id="39f18-507">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="39f18-507">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39f18-508">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-508">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-509">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="39f18-509">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="39f18-510">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="39f18-510">Az.MachineLearning</span></span>
* <span data-ttu-id="39f18-511">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="39f18-511">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="39f18-512">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39f18-512">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="39f18-513">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="39f18-513">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="39f18-514">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39f18-514">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="39f18-515">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39f18-515">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="39f18-516">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="39f18-516">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="39f18-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="39f18-517">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="39f18-518">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="39f18-518">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-519">Az.Network</span></span>
* <span data-ttu-id="39f18-520">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="39f18-520">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-521">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-521">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-522">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-522">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="39f18-523">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-523">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="39f18-524">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-524">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="39f18-525">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-525">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-526">Az.Resources</span></span>
* <span data-ttu-id="39f18-527">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="39f18-527">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-528">Az.Sql</span></span>
* <span data-ttu-id="39f18-529">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="39f18-529">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="39f18-530">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="39f18-530">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="39f18-531">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39f18-531">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="39f18-532">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="39f18-532">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-533">Az.Storage</span></span>
* <span data-ttu-id="39f18-534">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="39f18-534">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="39f18-535">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-535">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="39f18-536">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="39f18-536">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="39f18-537">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-537">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="39f18-538">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-538">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="39f18-539">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-539">General</span></span>
* <span data-ttu-id="39f18-540">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="39f18-540">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-541">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-541">Az.Accounts</span></span>
* <span data-ttu-id="39f18-542">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="39f18-542">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="39f18-543">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="39f18-543">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39f18-544">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39f18-544">Az.Batch</span></span>
* <span data-ttu-id="39f18-545">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="39f18-545">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-546">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-547">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="39f18-547">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39f18-548">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-548">Az.FrontDoor</span></span>
* <span data-ttu-id="39f18-549">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="39f18-549">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="39f18-550">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="39f18-550">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="39f18-551">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="39f18-551">Az.HealthcareApis</span></span>
* <span data-ttu-id="39f18-552">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="39f18-552">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-553">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-554">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="39f18-554">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="39f18-555">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="39f18-555">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="39f18-556">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="39f18-556">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-557">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-557">Az.Monitor</span></span>
* <span data-ttu-id="39f18-558">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="39f18-558">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="39f18-559">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="39f18-559">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="39f18-560">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="39f18-560">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-561">Az.Network</span></span>
* <span data-ttu-id="39f18-562">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="39f18-562">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-563">Az.Resources</span></span>
* <span data-ttu-id="39f18-564">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="39f18-564">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="39f18-565">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="39f18-565">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-566">Az.Sql</span></span>
* <span data-ttu-id="39f18-567">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="39f18-567">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-568">Az.Storage</span></span>
* <span data-ttu-id="39f18-569">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="39f18-569">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="39f18-570">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="39f18-570">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="39f18-571">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="39f18-571">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="39f18-572">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="39f18-572">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="39f18-573">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="39f18-573">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="39f18-574">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="39f18-574">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="39f18-575">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="39f18-575">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="39f18-576">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39f18-576">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="39f18-577">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39f18-577">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="39f18-578">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="39f18-578">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="39f18-579">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="39f18-579">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="39f18-580">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="39f18-580">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="39f18-581">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="39f18-581">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="39f18-582">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-582">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39f18-583">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="39f18-583">Highlights since the last major release</span></span>
* <span data-ttu-id="39f18-584">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-584">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="39f18-585">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-585">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-586">Az.Compute</span></span>
* <span data-ttu-id="39f18-587">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-587">VM Reapply feature</span></span>
    - <span data-ttu-id="39f18-588">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="39f18-588">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="39f18-589">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="39f18-589">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="39f18-590">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-590">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="39f18-591">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39f18-591">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="39f18-592">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-592">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="39f18-593">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="39f18-593">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="39f18-594">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="39f18-594">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="39f18-595">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="39f18-595">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="39f18-596">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="39f18-596">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="39f18-597">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-597">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="39f18-598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="39f18-598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="39f18-599">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="39f18-599">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="39f18-600">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="39f18-600">Get the Order</span></span>
* <span data-ttu-id="39f18-601">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="39f18-601">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="39f18-602">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="39f18-602">Create new Order</span></span>
* <span data-ttu-id="39f18-603">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="39f18-603">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="39f18-604">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="39f18-604">Remove the Order</span></span>
* <span data-ttu-id="39f18-605">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="39f18-605">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="39f18-606">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="39f18-606">Now creates Local Share</span></span>
* <span data-ttu-id="39f18-607">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="39f18-607">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="39f18-608">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="39f18-608">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="39f18-609">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="39f18-609">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="39f18-610">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="39f18-610">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="39f18-611">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="39f18-611">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="39f18-612">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="39f18-612">Gets the information about Triggers</span></span>
* <span data-ttu-id="39f18-613">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="39f18-613">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="39f18-614">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="39f18-614">Create new Triggers</span></span>
* <span data-ttu-id="39f18-615">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="39f18-615">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="39f18-616">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="39f18-616">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-617">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-618">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="39f18-618">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="39f18-619">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="39f18-619">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-620">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-620">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-621">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="39f18-621">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-622">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-622">Az.EventHub</span></span>
* <span data-ttu-id="39f18-623">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="39f18-623">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39f18-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-624">Az.FrontDoor</span></span>
* <span data-ttu-id="39f18-625">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="39f18-625">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="39f18-626">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="39f18-626">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="39f18-627">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="39f18-627">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="39f18-628">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="39f18-628">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-629">Az.Network</span></span>
* <span data-ttu-id="39f18-630">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="39f18-630">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="39f18-631">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="39f18-631">Az.PrivateDns</span></span>
* <span data-ttu-id="39f18-632">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-632">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-633">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-633">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-634">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="39f18-634">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="39f18-635">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="39f18-635">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="39f18-636">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-636">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39f18-637">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39f18-637">Az.RedisCache</span></span>
* <span data-ttu-id="39f18-638">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="39f18-638">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="39f18-639">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="39f18-639">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="39f18-640">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="39f18-640">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-641">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-641">Az.Resources</span></span>
- <span data-ttu-id="39f18-642">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="39f18-642">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="39f18-643">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="39f18-643">Updated create policy definition help example</span></span>
- <span data-ttu-id="39f18-644">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="39f18-644">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="39f18-645">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="39f18-645">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="39f18-646">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="39f18-646">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-647">Az.Sql</span></span>
* <span data-ttu-id="39f18-648">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="39f18-648">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="39f18-649">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="39f18-649">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="39f18-650">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-650">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="39f18-651">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-651">General</span></span>
* <span data-ttu-id="39f18-652">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-652">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-653">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-653">Az.Accounts</span></span>
* <span data-ttu-id="39f18-654">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="39f18-654">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="39f18-655">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="39f18-655">Az.Advisor</span></span>
* <span data-ttu-id="39f18-656">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="39f18-656">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39f18-657">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39f18-657">Az.Batch</span></span>
* <span data-ttu-id="39f18-658">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="39f18-658">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="39f18-659">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="39f18-659">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="39f18-660">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="39f18-660">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="39f18-661">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="39f18-661">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="39f18-662">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="39f18-662">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="39f18-663">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="39f18-663">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="39f18-664">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="39f18-664">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="39f18-665">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="39f18-665">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="39f18-666">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="39f18-666">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="39f18-667">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="39f18-667">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="39f18-668">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="39f18-668">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="39f18-669">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="39f18-669">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="39f18-670">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="39f18-670">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="39f18-671">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="39f18-671">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="39f18-672">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="39f18-672">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="39f18-673">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="39f18-673">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="39f18-674">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="39f18-674">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="39f18-675">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="39f18-675">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="39f18-676">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="39f18-676">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="39f18-677">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="39f18-677">This operation is no longer supported.</span></span>
* <span data-ttu-id="39f18-678">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="39f18-678">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="39f18-679">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="39f18-679">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="39f18-680">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="39f18-680">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="39f18-681">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="39f18-681">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="39f18-682">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="39f18-682">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="39f18-683">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="39f18-683">New non-verified images are also now returned.</span></span> <span data-ttu-id="39f18-684">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="39f18-684">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="39f18-685">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="39f18-685">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="39f18-686">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="39f18-686">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="39f18-687">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="39f18-687">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="39f18-688">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="39f18-688">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="39f18-689">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="39f18-689">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="39f18-690">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="39f18-690">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="39f18-691">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="39f18-691">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="39f18-692">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="39f18-692">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="39f18-693">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="39f18-693">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-694">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-694">Az.Cdn</span></span>
* <span data-ttu-id="39f18-695">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="39f18-695">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="39f18-696">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="39f18-696">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-697">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-697">Az.Compute</span></span>
* <span data-ttu-id="39f18-698">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="39f18-698">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="39f18-699">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="39f18-699">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="39f18-700">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="39f18-700">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="39f18-701">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-701">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="39f18-702">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-702">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="39f18-703">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="39f18-703">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="39f18-704">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-704">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="39f18-705">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="39f18-705">Breaking changes</span></span>
    - <span data-ttu-id="39f18-706">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="39f18-706">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="39f18-707">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="39f18-707">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-708">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-708">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-709">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="39f18-709">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-711">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="39f18-711">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="39f18-712">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="39f18-712">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="39f18-713">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="39f18-713">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="39f18-714">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="39f18-714">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="39f18-715">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="39f18-715">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="39f18-716">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="39f18-716">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39f18-717">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-717">Az.FrontDoor</span></span>
* <span data-ttu-id="39f18-718">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="39f18-718">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39f18-719">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-719">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-720">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="39f18-720">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="39f18-721">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="39f18-721">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="39f18-722">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="39f18-722">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="39f18-723">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-723">Removed five cmdlets:</span></span>
    - <span data-ttu-id="39f18-724">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="39f18-724">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="39f18-725">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="39f18-725">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="39f18-726">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="39f18-726">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="39f18-727">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39f18-727">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="39f18-728">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39f18-728">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="39f18-729">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-729">Added three cmdlets:</span></span>
    - <span data-ttu-id="39f18-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="39f18-730">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="39f18-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="39f18-731">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="39f18-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="39f18-732">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="39f18-733">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="39f18-733">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="39f18-734">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="39f18-734">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="39f18-735">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="39f18-735">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="39f18-736">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="39f18-736">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="39f18-737">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="39f18-737">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="39f18-738">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="39f18-738">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="39f18-739">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="39f18-739">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="39f18-740">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="39f18-740">Added some scenario test cases.</span></span>
* <span data-ttu-id="39f18-741">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="39f18-741">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-742">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-742">Az.IotHub</span></span>
* <span data-ttu-id="39f18-743">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="39f18-743">Breaking changes:</span></span>
    - <span data-ttu-id="39f18-744">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="39f18-744">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39f18-745">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="39f18-745">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="39f18-746">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="39f18-746">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39f18-747">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="39f18-747">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="39f18-748">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="39f18-748">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="39f18-749">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="39f18-749">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="39f18-750">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="39f18-750">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="39f18-751">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="39f18-751">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="39f18-752">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="39f18-752">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39f18-753">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="39f18-753">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="39f18-754">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="39f18-754">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="39f18-755">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="39f18-755">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-756">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-756">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-757">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-757">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-758">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-758">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="39f18-759">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-759">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="39f18-760">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-760">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-761">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-761">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-762">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-762">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-763">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-763">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-764">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-764">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-765">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="39f18-765">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-766">Az.Resources</span></span>
* <span data-ttu-id="39f18-767">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="39f18-767">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-768">Az.Network</span></span>
* <span data-ttu-id="39f18-769">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="39f18-769">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="39f18-770">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="39f18-770">Updated cmdlet:</span></span>
        - <span data-ttu-id="39f18-771">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-771">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-772">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-772">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-773">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-773">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-774">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-774">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-775">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-775">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="39f18-776">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="39f18-776">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="39f18-777">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-777">New cmdlet:</span></span>
        - <span data-ttu-id="39f18-778">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="39f18-778">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="39f18-779">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="39f18-779">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="39f18-780">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-780">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="39f18-781">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-781">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="39f18-782">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="39f18-782">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="39f18-783">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="39f18-783">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="39f18-784">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-784">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="39f18-785">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="39f18-785">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="39f18-786">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-786">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-787">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="39f18-787">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="39f18-788">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="39f18-788">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="39f18-789">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="39f18-789">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="39f18-790">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="39f18-790">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="39f18-791">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="39f18-791">Set-AzVirtualHub</span></span>
* <span data-ttu-id="39f18-792">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="39f18-792">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="39f18-793">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="39f18-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39f18-794">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="39f18-794">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="39f18-795">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="39f18-795">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="39f18-796">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="39f18-796">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="39f18-797">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="39f18-797">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="39f18-798">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-798">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="39f18-799">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-799">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-800">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-800">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="39f18-801">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="39f18-801">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39f18-802">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="39f18-802">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39f18-803">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="39f18-803">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39f18-804">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="39f18-804">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39f18-805">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="39f18-805">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="39f18-806">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="39f18-806">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="39f18-807">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="39f18-807">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="39f18-808">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-808">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-809">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="39f18-809">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="39f18-810">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="39f18-810">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="39f18-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="39f18-811">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="39f18-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="39f18-812">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="39f18-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="39f18-813">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="39f18-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-814">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="39f18-815">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="39f18-815">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39f18-816">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="39f18-816">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="39f18-817">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="39f18-817">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="39f18-818">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="39f18-818">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="39f18-819">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="39f18-819">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="39f18-820">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="39f18-820">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="39f18-821">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="39f18-821">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="39f18-822">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="39f18-822">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="39f18-823">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="39f18-823">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="39f18-824">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-824">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="39f18-825">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-825">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="39f18-826">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-826">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-827">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-827">New-AzIpGroup</span></span>
        - <span data-ttu-id="39f18-828">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-828">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="39f18-829">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-829">Get-AzIpGroup</span></span>
        - <span data-ttu-id="39f18-830">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-830">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-831">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-831">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-832">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="39f18-832">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-833">Az.Sql</span></span>
* <span data-ttu-id="39f18-834">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="39f18-834">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="39f18-835">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="39f18-835">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="39f18-836">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="39f18-836">Removed deprecated aliases:</span></span>
* <span data-ttu-id="39f18-837">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="39f18-837">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="39f18-838">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="39f18-838">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="39f18-839">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-839">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="39f18-840">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="39f18-840">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="39f18-841">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="39f18-841">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="39f18-842">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="39f18-842">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-843">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-843">Az.Storage</span></span>
* <span data-ttu-id="39f18-844">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="39f18-844">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="39f18-845">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-845">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="39f18-846">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-846">Set-AzStorageAccount</span></span>
* <span data-ttu-id="39f18-847">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="39f18-847">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="39f18-848">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39f18-848">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="39f18-849">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39f18-849">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="39f18-850">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-850">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="39f18-851">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-851">General</span></span>
* <span data-ttu-id="39f18-852">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-852">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-853">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-853">Az.Accounts</span></span>
* <span data-ttu-id="39f18-854">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="39f18-854">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39f18-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-855">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-856">**Set-AzApiManagementApi** : aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="39f18-856">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="39f18-857">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="39f18-857">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-858">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-858">Az.Automation</span></span>
* <span data-ttu-id="39f18-859">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="39f18-859">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39f18-860">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39f18-860">Az.Batch</span></span>
* <span data-ttu-id="39f18-861">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="39f18-861">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-862">Az.Compute</span></span>
* <span data-ttu-id="39f18-863">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-863">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="39f18-864">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="39f18-864">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="39f18-865">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="39f18-865">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="39f18-866">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="39f18-866">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-867">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-868">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="39f18-868">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="39f18-869">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="39f18-869">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="39f18-870">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="39f18-870">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-871">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-871">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-872">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="39f18-872">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="39f18-873">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="39f18-873">Az.HealthcareApis</span></span>
* <span data-ttu-id="39f18-874">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-874">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="39f18-875">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="39f18-875">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="39f18-876">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="39f18-876">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="39f18-877">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="39f18-877">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-878">Az.IotHub</span></span>
* <span data-ttu-id="39f18-879">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="39f18-879">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="39f18-880">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="39f18-880">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-881">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-881">Az.Monitor</span></span>
* <span data-ttu-id="39f18-882">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="39f18-882">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="39f18-883">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="39f18-883">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="39f18-884">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="39f18-884">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="39f18-885">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="39f18-885">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-886">Az.Network</span></span>
* <span data-ttu-id="39f18-887">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="39f18-887">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="39f18-888">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-888">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="39f18-889">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-889">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-890">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-890">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="39f18-891">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-891">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="39f18-892">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="39f18-892">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="39f18-893">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-893">Updated cmdlets:</span></span>
        - <span data-ttu-id="39f18-894">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-894">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39f18-895">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-895">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39f18-896">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-896">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="39f18-897">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="39f18-897">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="39f18-898">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="39f18-898">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="39f18-899">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="39f18-899">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="39f18-900">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="39f18-900">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39f18-901">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39f18-901">Az.RedisCache</span></span>
* <span data-ttu-id="39f18-902">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="39f18-902">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-903">Az.Sql</span></span>
* <span data-ttu-id="39f18-904">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="39f18-904">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-905">Az.Storage</span></span>
* <span data-ttu-id="39f18-906">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="39f18-906">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="39f18-907">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="39f18-907">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="39f18-908">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="39f18-908">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="39f18-909">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="39f18-909">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="39f18-910">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-910">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39f18-911">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39f18-911">Az.StorageSync</span></span>
* <span data-ttu-id="39f18-912">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="39f18-912">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-913">Az.Websites</span></span>
* <span data-ttu-id="39f18-914">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="39f18-914">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="39f18-915">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-915">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="39f18-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-916">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-917">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="39f18-917">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="39f18-918">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="39f18-918">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="39f18-919">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="39f18-919">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-920">Az.Automation</span></span>
* <span data-ttu-id="39f18-921">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="39f18-921">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="39f18-922">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="39f18-922">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="39f18-923">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="39f18-923">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-924">Az.Compute</span></span>
* <span data-ttu-id="39f18-925">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-925">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="39f18-926">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-926">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="39f18-927">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="39f18-927">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="39f18-928">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="39f18-928">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="39f18-929">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="39f18-929">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="39f18-930">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="39f18-930">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="39f18-931">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="39f18-931">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="39f18-932">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="39f18-932">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="39f18-933">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="39f18-933">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-934">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-934">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-935">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="39f18-935">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="39f18-936">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="39f18-936">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39f18-937">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-937">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-938">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="39f18-938">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-939">Az.IotHub</span></span>
* <span data-ttu-id="39f18-940">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="39f18-940">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="39f18-941">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="39f18-941">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="39f18-942">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="39f18-942">New cmdlets are:</span></span>
    - <span data-ttu-id="39f18-943">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39f18-943">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="39f18-944">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39f18-944">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="39f18-945">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39f18-945">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="39f18-946">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="39f18-946">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-947">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-947">Az.Monitor</span></span>
* <span data-ttu-id="39f18-948">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="39f18-948">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="39f18-949">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="39f18-949">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="39f18-950">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="39f18-950">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="39f18-951">La versione API delle richieste **ActionGroups** è ora **2019-06-01** , prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="39f18-951">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="39f18-952">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="39f18-952">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="39f18-953">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="39f18-953">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="39f18-954">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f18-954">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="39f18-955">**NOTA** : questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="39f18-955">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="39f18-956">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource** ) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="39f18-956">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="39f18-957">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="39f18-957">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="39f18-958">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource** ) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="39f18-958">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="39f18-959">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="39f18-959">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="39f18-960">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="39f18-960">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="39f18-961">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="39f18-961">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="39f18-962">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="39f18-962">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="39f18-963">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="39f18-963">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="39f18-964">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="39f18-964">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="39f18-965">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-965">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="39f18-966">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="39f18-966">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="39f18-967">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-967">Overall improved help files</span></span>
* <span data-ttu-id="39f18-968">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="39f18-968">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-969">Az.Network</span></span>
* <span data-ttu-id="39f18-970">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="39f18-970">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="39f18-971">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="39f18-971">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="39f18-972">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="39f18-972">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="39f18-973">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="39f18-973">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="39f18-974">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="39f18-974">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="39f18-975">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="39f18-975">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="39f18-976">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="39f18-976">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="39f18-977">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39f18-977">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="39f18-978">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-978">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="39f18-979">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="39f18-979">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="39f18-980">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-980">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="39f18-981">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-981">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="39f18-982">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-982">New cmdlets</span></span>
        - <span data-ttu-id="39f18-983">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="39f18-983">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="39f18-984">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-984">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="39f18-985">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="39f18-985">Updated cmdlet:</span></span>
        - <span data-ttu-id="39f18-986">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="39f18-986">New-VpnSite</span></span>
        - <span data-ttu-id="39f18-987">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="39f18-987">Update-VpnSite</span></span>
        - <span data-ttu-id="39f18-988">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-988">New-VpnConnection</span></span>
        - <span data-ttu-id="39f18-989">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-989">Update-VpnConnection</span></span>
* <span data-ttu-id="39f18-990">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="39f18-990">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-992">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="39f18-992">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="39f18-993">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="39f18-993">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-994">Az.Resources</span></span>
* <span data-ttu-id="39f18-995">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="39f18-995">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-996">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-996">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-997">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="39f18-997">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="39f18-998">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="39f18-998">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="39f18-999">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39f18-999">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39f18-1000">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="39f18-1000">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="39f18-1001">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39f18-1001">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="39f18-1002">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="39f18-1002">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="39f18-1003">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39f18-1003">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39f18-1004">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39f18-1004">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39f18-1005">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="39f18-1005">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="39f18-1006">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39f18-1006">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="39f18-1007">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="39f18-1007">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="39f18-1008">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="39f18-1008">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="39f18-1009">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="39f18-1009">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="39f18-1010">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="39f18-1010">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="39f18-1011">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="39f18-1011">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="39f18-1012">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="39f18-1012">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="39f18-1013">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="39f18-1013">Az.SignalR</span></span>
* <span data-ttu-id="39f18-1014">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="39f18-1014">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1015">Az.Sql</span></span>
* <span data-ttu-id="39f18-1016">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="39f18-1016">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="39f18-1017">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="39f18-1017">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="39f18-1018">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1018">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="39f18-1019">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="39f18-1019">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="39f18-1020">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="39f18-1020">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1021">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1021">Az.Storage</span></span>
* <span data-ttu-id="39f18-1022">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="39f18-1022">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="39f18-1023">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1023">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="39f18-1024">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1024">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="39f18-1025">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1025">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="39f18-1026">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="39f18-1026">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="39f18-1027">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1027">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="39f18-1028">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="39f18-1028">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="39f18-1029">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39f18-1029">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="39f18-1030">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39f18-1030">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="39f18-1031">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39f18-1031">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="39f18-1032">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="39f18-1032">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1033">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1033">Az.Websites</span></span>
* <span data-ttu-id="39f18-1034">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="39f18-1034">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="39f18-1035">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="39f18-1035">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="39f18-1036">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="39f18-1036">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="39f18-1037">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1037">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="39f18-1038">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-1038">General</span></span>
* <span data-ttu-id="39f18-1039">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="39f18-1039">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1040">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1041">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="39f18-1041">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="39f18-1042">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="39f18-1042">Az.Aks</span></span>
* <span data-ttu-id="39f18-1043">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="39f18-1043">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="39f18-1044">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="39f18-1044">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39f18-1045">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-1045">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-1046">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="39f18-1046">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="39f18-1047">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="39f18-1047">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="39f18-1048">**Get-AzApiManagementProduct** : aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="39f18-1048">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="39f18-1049">**New-AzApiManagementApiRevision** : correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="39f18-1049">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="39f18-1050">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="39f18-1050">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39f18-1051">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39f18-1051">Az.Batch</span></span>
* <span data-ttu-id="39f18-1052">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="39f18-1052">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-1053">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-1053">Az.Cdn</span></span>
* <span data-ttu-id="39f18-1054">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="39f18-1054">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1055">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1055">Az.Compute</span></span>
* <span data-ttu-id="39f18-1056">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1056">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="39f18-1057">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-1057">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="39f18-1058">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-1058">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="39f18-1059">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-1059">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="39f18-1060">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="39f18-1060">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="39f18-1061">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39f18-1061">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="39f18-1062">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="39f18-1062">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="39f18-1063">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="39f18-1063">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1064">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1064">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1065">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="39f18-1065">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="39f18-1066">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="39f18-1066">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="39f18-1067">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="39f18-1067">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="39f18-1068">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="39f18-1068">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-1069">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-1070">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="39f18-1070">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-1071">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1071">Az.EventHub</span></span>
* <span data-ttu-id="39f18-1072">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-1072">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="39f18-1073">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="39f18-1073">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="39f18-1074">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="39f18-1074">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="39f18-1075">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="39f18-1075">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="39f18-1076">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="39f18-1076">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="39f18-1077">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="39f18-1077">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-1078">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-1078">Az.Monitor</span></span>
* <span data-ttu-id="39f18-1079">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-1079">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1080">Az.Network</span></span>
* <span data-ttu-id="39f18-1081">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1081">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="39f18-1082">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="39f18-1082">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="39f18-1083">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="39f18-1083">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="39f18-1084">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="39f18-1084">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="39f18-1085">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="39f18-1085">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="39f18-1086">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="39f18-1086">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="39f18-1087">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="39f18-1087">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-1088">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1088">Az.OperationalInsights</span></span>
* <span data-ttu-id="39f18-1089">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="39f18-1089">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="39f18-1090">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="39f18-1090">Added example</span></span>
    - <span data-ttu-id="39f18-1091">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="39f18-1091">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="39f18-1092">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="39f18-1092">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="39f18-1093">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="39f18-1093">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1094">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1094">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1095">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1095">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1096">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1096">Az.Resources</span></span>
* <span data-ttu-id="39f18-1097">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="39f18-1097">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="39f18-1098">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="39f18-1098">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="39f18-1099">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="39f18-1099">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="39f18-1100">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-1100">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39f18-1101">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39f18-1101">Az.ServiceBus</span></span>
* <span data-ttu-id="39f18-1102">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-1102">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="39f18-1103">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="39f18-1103">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="39f18-1104">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="39f18-1104">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-1105">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-1105">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-1106">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="39f18-1106">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="39f18-1107">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="39f18-1107">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="39f18-1108">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="39f18-1108">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="39f18-1109">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="39f18-1109">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="39f18-1110">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="39f18-1110">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="39f18-1111">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="39f18-1111">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1112">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1112">Az.Sql</span></span>
* <span data-ttu-id="39f18-1113">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="39f18-1113">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1114">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1114">Az.Storage</span></span>
* <span data-ttu-id="39f18-1115">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="39f18-1115">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="39f18-1116">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="39f18-1116">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="39f18-1117">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1117">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="39f18-1118">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39f18-1118">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="39f18-1119">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="39f18-1119">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="39f18-1120">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39f18-1120">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1121">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1121">Az.Websites</span></span>
* <span data-ttu-id="39f18-1122">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39f18-1122">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="39f18-1123">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1123">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1124">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1125">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39f18-1125">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="39f18-1126">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1126">Az.ApplicationInsights</span></span>
* <span data-ttu-id="39f18-1127">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="39f18-1127">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1128">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1128">Az.Automation</span></span>
* <span data-ttu-id="39f18-1129">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="39f18-1129">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-1130">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1130">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-1131">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="39f18-1131">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1132">Az.Compute</span></span>
* <span data-ttu-id="39f18-1133">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="39f18-1133">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="39f18-1134">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="39f18-1134">Az.ContainerRegistry</span></span>
* <span data-ttu-id="39f18-1135">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="39f18-1135">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="39f18-1136">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="39f18-1136">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1137">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1137">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1138">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="39f18-1138">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="39f18-1139">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="39f18-1139">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-1140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1140">Az.EventHub</span></span>
* <span data-ttu-id="39f18-1141">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="39f18-1141">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="39f18-1142">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="39f18-1142">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-1143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-1143">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-1144">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="39f18-1144">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39f18-1145">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1145">Az.LogicApp</span></span>
* <span data-ttu-id="39f18-1146">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="39f18-1146">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="39f18-1147">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="39f18-1147">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="39f18-1148">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1148">Az.ManagedServices</span></span>
* <span data-ttu-id="39f18-1149">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="39f18-1149">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1150">Az.Network</span></span>
* <span data-ttu-id="39f18-1151">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="39f18-1151">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="39f18-1152">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-1152">New cmdlets</span></span>
        - <span data-ttu-id="39f18-1153">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f18-1153">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39f18-1154">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-1154">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39f18-1155">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1155">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-1156">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1156">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-1157">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1157">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-1158">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1158">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="39f18-1159">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="39f18-1159">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="39f18-1160">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-1160">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="39f18-1161">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="39f18-1161">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="39f18-1162">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1162">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="39f18-1163">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="39f18-1163">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="39f18-1164">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="39f18-1164">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="39f18-1165">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="39f18-1165">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="39f18-1166">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="39f18-1166">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="39f18-1167">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-1167">Updated cmdlets</span></span>
        - <span data-ttu-id="39f18-1168">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1168">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39f18-1169">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1169">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="39f18-1170">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1170">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="39f18-1171">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1171">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="39f18-1172">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1172">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="39f18-1173">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="39f18-1173">Updated cmdlet:</span></span>
        - <span data-ttu-id="39f18-1174">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1174">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="39f18-1175">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1175">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="39f18-1176">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1176">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="39f18-1177">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="39f18-1177">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="39f18-1178">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="39f18-1178">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="39f18-1179">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="39f18-1179">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-1180">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1180">Az.OperationalInsights</span></span>
* <span data-ttu-id="39f18-1181">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="39f18-1181">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="39f18-1182">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="39f18-1182">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1183">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1184">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1184">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="39f18-1185">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1185">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="39f18-1186">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1186">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="39f18-1187">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1187">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="39f18-1188">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1188">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="39f18-1189">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1189">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="39f18-1190">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1190">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="39f18-1191">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1191">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="39f18-1192">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1192">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="39f18-1193">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="39f18-1193">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1194">Az.Resources</span></span>
- <span data-ttu-id="39f18-1195">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="39f18-1195">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="39f18-1196">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="39f18-1196">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39f18-1197">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39f18-1197">Az.ServiceBus</span></span>
* <span data-ttu-id="39f18-1198">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="39f18-1198">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="39f18-1199">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="39f18-1199">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1200">Az.Sql</span></span>
* <span data-ttu-id="39f18-1201">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="39f18-1201">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="39f18-1202">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="39f18-1202">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="39f18-1203">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="39f18-1203">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1204">Az.Storage</span></span>
* <span data-ttu-id="39f18-1205">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="39f18-1205">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39f18-1206">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39f18-1206">Az.StorageSync</span></span>
* <span data-ttu-id="39f18-1207">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="39f18-1207">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="39f18-1208">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="39f18-1208">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1209">Az.Websites</span></span>
* <span data-ttu-id="39f18-1210">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1210">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="39f18-1211">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1211">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="39f18-1212">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="39f18-1212">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="39f18-1213">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1213">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1214">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1215">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="39f18-1215">Add support for profile cmdlets</span></span>
* <span data-ttu-id="39f18-1216">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="39f18-1216">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="39f18-1217">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="39f18-1217">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="39f18-1218">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="39f18-1218">Az.Advisor</span></span>
* <span data-ttu-id="39f18-1219">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="39f18-1219">GA release of Az.Advisor</span></span>
* <span data-ttu-id="39f18-1220">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="39f18-1220">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="39f18-1221">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-1221">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-1222">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="39f18-1222">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="39f18-1223">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="39f18-1223">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="39f18-1224">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="39f18-1224">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="39f18-1225">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="39f18-1225">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="39f18-1226">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="39f18-1226">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="39f18-1227">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39f18-1227">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="39f18-1228">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="39f18-1228">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1229">Az.Automation</span></span>
* <span data-ttu-id="39f18-1230">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="39f18-1230">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1231">Az.Compute</span></span>
* <span data-ttu-id="39f18-1232">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1232">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1233">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1234">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="39f18-1234">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39f18-1235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39f18-1235">Az.EventGrid</span></span>
* <span data-ttu-id="39f18-1236">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="39f18-1236">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-1237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1237">Az.IotHub</span></span>
* <span data-ttu-id="39f18-1238">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1238">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1239">Az.Network</span></span>
* <span data-ttu-id="39f18-1240">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="39f18-1240">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="39f18-1241">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="39f18-1241">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-1242">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1242">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-1243">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="39f18-1243">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="39f18-1244">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="39f18-1244">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-1245">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1245">Az.OperationalInsights</span></span>
* <span data-ttu-id="39f18-1246">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="39f18-1246">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1247">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1248">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="39f18-1248">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1249">Az.Resources</span></span>
    - <span data-ttu-id="39f18-1250">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="39f18-1250">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="39f18-1251">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="39f18-1251">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="39f18-1252">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="39f18-1252">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="39f18-1253">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="39f18-1253">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39f18-1254">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39f18-1254">Az.ServiceBus</span></span>
* <span data-ttu-id="39f18-1255">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="39f18-1255">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1256">Az.Sql</span></span>
* <span data-ttu-id="39f18-1257">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="39f18-1257">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="39f18-1258">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1258">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="39f18-1259">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="39f18-1259">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="39f18-1260">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="39f18-1260">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="39f18-1261">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="39f18-1261">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="39f18-1262">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="39f18-1262">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="39f18-1263">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="39f18-1263">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="39f18-1264">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="39f18-1264">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="39f18-1265">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="39f18-1265">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1266">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1266">Az.Storage</span></span>
* <span data-ttu-id="39f18-1267">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-1267">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="39f18-1268">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="39f18-1268">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="39f18-1269">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="39f18-1269">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="39f18-1270">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="39f18-1270">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="39f18-1271">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1271">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="39f18-1272">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1272">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="39f18-1273">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1273">Set-AzStorageAccount</span></span>
* <span data-ttu-id="39f18-1274">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="39f18-1274">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="39f18-1275">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39f18-1275">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="39f18-1276">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="39f18-1276">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="39f18-1277">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="39f18-1277">Az.StorageSync</span></span>
* <span data-ttu-id="39f18-1278">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="39f18-1278">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="39f18-1279">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1279">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1280">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1280">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1281">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="39f18-1281">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="39f18-1282">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="39f18-1282">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="39f18-1283">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="39f18-1283">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="39f18-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="39f18-1284">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="39f18-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="39f18-1285">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1286">Az.Compute</span></span>
* <span data-ttu-id="39f18-1287">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1287">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="39f18-1288">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="39f18-1288">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="39f18-1289">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="39f18-1289">Az.Dns</span></span>
* <span data-ttu-id="39f18-1290">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1290">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39f18-1291">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39f18-1291">Az.EventGrid</span></span>
* <span data-ttu-id="39f18-1292">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="39f18-1292">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="39f18-1293">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-1293">New cmdlets:</span></span>
    - <span data-ttu-id="39f18-1294">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="39f18-1294">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="39f18-1295">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1295">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="39f18-1296">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="39f18-1296">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="39f18-1297">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1297">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="39f18-1298">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="39f18-1298">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="39f18-1299">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1299">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="39f18-1300">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="39f18-1300">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="39f18-1301">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1301">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="39f18-1302">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="39f18-1302">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="39f18-1303">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="39f18-1303">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="39f18-1304">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="39f18-1304">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="39f18-1305">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1305">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="39f18-1306">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="39f18-1306">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="39f18-1307">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1307">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="39f18-1308">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="39f18-1308">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="39f18-1309">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="39f18-1309">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="39f18-1310">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-1310">Updated cmdlets:</span></span>
    - <span data-ttu-id="39f18-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="39f18-1311">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="39f18-1312">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="39f18-1312">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="39f18-1313">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="39f18-1313">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="39f18-1314">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="39f18-1314">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="39f18-1315">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="39f18-1315">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="39f18-1316">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="39f18-1316">Event subscription expiration date,</span></span>
            - <span data-ttu-id="39f18-1317">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1317">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="39f18-1318">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1318">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="39f18-1319">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1319">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="39f18-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="39f18-1320">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="39f18-1321">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1321">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="39f18-1322">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="39f18-1322">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="39f18-1323">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="39f18-1323">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="39f18-1324">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="39f18-1324">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39f18-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="39f18-1326">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="39f18-1326">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="39f18-1327">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="39f18-1327">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="39f18-1328">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="39f18-1328">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="39f18-1329">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="39f18-1329">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1330">Az.Network</span></span>
* <span data-ttu-id="39f18-1331">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-1331">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="39f18-1332">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-1332">New cmdlets</span></span>
        - <span data-ttu-id="39f18-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="39f18-1333">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="39f18-1334">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="39f18-1334">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="39f18-1335">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-1335">New cmdlets</span></span>
        - <span data-ttu-id="39f18-1336">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="39f18-1336">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="39f18-1337">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-1337">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="39f18-1338">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-1338">New cmdlets</span></span>
        - <span data-ttu-id="39f18-1339">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-1339">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39f18-1340">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-1340">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39f18-1341">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="39f18-1341">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="39f18-1342">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1342">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="39f18-1343">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1343">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="39f18-1344">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f18-1344">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="39f18-1345">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-1345">New cmdlets</span></span>
        - <span data-ttu-id="39f18-1346">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f18-1346">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39f18-1347">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f18-1347">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39f18-1348">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f18-1348">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="39f18-1349">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1349">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="39f18-1350">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="39f18-1350">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="39f18-1351">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="39f18-1351">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="39f18-1352">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="39f18-1352">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="39f18-1353">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="39f18-1353">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="39f18-1354">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="39f18-1354">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="39f18-1355">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="39f18-1355">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="39f18-1356">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1356">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="39f18-1357">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="39f18-1357">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="39f18-1358">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1358">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="39f18-1359">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="39f18-1359">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="39f18-1360">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-1360">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="39f18-1361">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-1361">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="39f18-1362">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="39f18-1362">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="39f18-1363">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1363">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="39f18-1364">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="39f18-1364">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="39f18-1365">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="39f18-1365">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="39f18-1366">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-1366">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="39f18-1367">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="39f18-1367">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="39f18-1368">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="39f18-1368">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="39f18-1369">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39f18-1369">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="39f18-1370">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1370">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="39f18-1371">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1371">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="39f18-1372">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1372">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-1373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1373">Az.OperationalInsights</span></span>
* <span data-ttu-id="39f18-1374">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="39f18-1374">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1375">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1375">Az.Resources</span></span>
* <span data-ttu-id="39f18-1376">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="39f18-1376">Support for additional Template Export options</span></span>
    - <span data-ttu-id="39f18-1377">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-1377">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="39f18-1378">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-1378">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="39f18-1379">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="39f18-1379">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-1380">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-1380">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-1381">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="39f18-1381">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1382">Az.Sql</span></span>
* <span data-ttu-id="39f18-1383">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="39f18-1383">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="39f18-1384">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="39f18-1384">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="39f18-1385">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="39f18-1385">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="39f18-1386">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39f18-1386">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="39f18-1387">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39f18-1387">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="39f18-1388">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="39f18-1388">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="39f18-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="39f18-1389">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="39f18-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="39f18-1390">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1391">Az.Storage</span></span>
* <span data-ttu-id="39f18-1392">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1392">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="39f18-1393">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1393">New-AzStorageAccount</span></span>
* <span data-ttu-id="39f18-1394">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="39f18-1394">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="39f18-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1395">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1396">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1396">Az.Websites</span></span>
* <span data-ttu-id="39f18-1397">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="39f18-1397">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="39f18-1398">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="39f18-1398">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="39f18-1399">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1399">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="39f18-1400">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-1400">Az.Cdn</span></span>
* <span data-ttu-id="39f18-1401">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="39f18-1401">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1402">Az.Compute</span></span>
* <span data-ttu-id="39f18-1403">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1403">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="39f18-1404">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="39f18-1404">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-1405">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1405">Az.EventHub</span></span>
* <span data-ttu-id="39f18-1406">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="39f18-1406">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="39f18-1407">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f18-1407">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1408">Az.Network</span></span>
* <span data-ttu-id="39f18-1409">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="39f18-1409">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="39f18-1410">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="39f18-1410">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-1411">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1411">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-1412">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="39f18-1412">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1413">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1414">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="39f18-1414">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39f18-1415">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39f18-1415">Az.ServiceBus</span></span>
* <span data-ttu-id="39f18-1416">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f18-1416">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-1417">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-1417">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-1418">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="39f18-1418">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="39f18-1419">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="39f18-1419">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1420">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1420">Az.Sql</span></span>
* <span data-ttu-id="39f18-1421">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="39f18-1421">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="39f18-1422">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1422">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="39f18-1423">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="39f18-1423">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="39f18-1424">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="39f18-1424">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1425">Az.Websites</span></span>
* <span data-ttu-id="39f18-1426">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="39f18-1426">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="39f18-1427">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1427">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="39f18-1428">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-1428">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-1429">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="39f18-1429">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="39f18-1430">**Get-AzApiManagementDiagnostic** : ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1430">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="39f18-1431">**New-AzApiManagementDiagnostic** : crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1431">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="39f18-1432">**New-AzApiManagementHttpMessageDiagnostic** : crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="39f18-1432">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="39f18-1433">**New-AzApiManagementPipelineDiagnosticSetting** : crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1433">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="39f18-1434">**New-AzApiManagementSamplingSetting** : crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="39f18-1434">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="39f18-1435">**Remove-AzApiManagementDiagnostic** : rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1435">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="39f18-1436">**Set-AzApiManagementDiagnostic** : aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1436">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="39f18-1437">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-1437">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="39f18-1438">**Get-AzApiManagementCache** : ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="39f18-1438">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="39f18-1439">**New-AzApiManagementCache** : crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1439">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="39f18-1440">**Remove-AzApiManagementCache** : rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="39f18-1440">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="39f18-1441">**Update-AzApiManagementCache** : aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="39f18-1441">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="39f18-1442">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1442">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="39f18-1443">**New-AzApiManagementSchema** : crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1443">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="39f18-1444">**Get-AzApiManagementSchema** : ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1444">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="39f18-1445">**Remove-AzApiManagementSchema** : rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1445">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="39f18-1446">**Set-AzApiManagementSchema** : aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="39f18-1446">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="39f18-1447">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="39f18-1447">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="39f18-1448">**New-AzApiManagementUserToken** : genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1448">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="39f18-1449">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="39f18-1449">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="39f18-1450">**Get-AzApiManagementNetworkStatus** : ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="39f18-1450">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="39f18-1451">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="39f18-1451">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="39f18-1452">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-1452">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="39f18-1453">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="39f18-1453">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="39f18-1454">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="39f18-1454">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="39f18-1455">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1455">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="39f18-1456">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="39f18-1456">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="39f18-1457">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="39f18-1457">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="39f18-1458">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="39f18-1458">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="39f18-1459">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="39f18-1459">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="39f18-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="39f18-1460">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="39f18-1461">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="39f18-1461">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="39f18-1462">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39f18-1462">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="39f18-1463">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="39f18-1463">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="39f18-1464">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="39f18-1464">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="39f18-1465">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="39f18-1465">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="39f18-1466">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="39f18-1466">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="39f18-1467">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="39f18-1467">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="39f18-1468">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39f18-1468">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="39f18-1469">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1469">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="39f18-1470">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39f18-1470">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="39f18-1471">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1471">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="39f18-1472">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="39f18-1472">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="39f18-1473">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="39f18-1473">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="39f18-1474">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1474">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="39f18-1475">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39f18-1475">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="39f18-1476">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="39f18-1476">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="39f18-1477">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="39f18-1477">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="39f18-1478">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1478">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="39f18-1479">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="39f18-1479">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="39f18-1480">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="39f18-1480">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="39f18-1481">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="39f18-1481">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="39f18-1482">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="39f18-1482">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="39f18-1483">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="39f18-1483">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="39f18-1484">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="39f18-1484">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="39f18-1485">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="39f18-1485">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="39f18-1486">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39f18-1486">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="39f18-1487">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39f18-1487">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="39f18-1488">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1488">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="39f18-1489">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="39f18-1489">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="39f18-1490">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39f18-1490">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="39f18-1491">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="39f18-1491">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="39f18-1492">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1492">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="39f18-1493">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="39f18-1493">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="39f18-1494">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="39f18-1494">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="39f18-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="39f18-1495">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="39f18-1496">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="39f18-1496">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="39f18-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="39f18-1497">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="39f18-1498">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39f18-1498">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="39f18-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="39f18-1499">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="39f18-1500">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="39f18-1500">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="39f18-1501">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="39f18-1501">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="39f18-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="39f18-1502">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="39f18-1503">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="39f18-1503">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="39f18-1504">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="39f18-1504">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="39f18-1505">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="39f18-1505">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1506">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1506">Az.Automation</span></span>
* <span data-ttu-id="39f18-1507">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="39f18-1507">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="39f18-1508">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="39f18-1508">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="39f18-1509">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="39f18-1509">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="39f18-1510">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="39f18-1510">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="39f18-1511">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="39f18-1511">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="39f18-1512">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="39f18-1512">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="39f18-1513">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="39f18-1513">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1514">Az.Compute</span></span>
* <span data-ttu-id="39f18-1515">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="39f18-1515">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="39f18-1516">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="39f18-1516">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-1517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-1517">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-1518">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1518">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-1519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-1519">Az.Monitor</span></span>
* <span data-ttu-id="39f18-1520">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-1520">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1521">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1521">Az.Network</span></span>
* <span data-ttu-id="39f18-1522">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="39f18-1522">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="39f18-1523">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="39f18-1523">Updated cmdlet:</span></span>
        - <span data-ttu-id="39f18-1524">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="39f18-1524">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="39f18-1525">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="39f18-1525">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1526">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1526">Az.Resources</span></span>
* <span data-ttu-id="39f18-1527">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="39f18-1527">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1528">Az.Sql</span></span>
* <span data-ttu-id="39f18-1529">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="39f18-1529">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="39f18-1530">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1530">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1531">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1532">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="39f18-1532">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-1533">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1533">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-1534">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="39f18-1534">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="39f18-1535">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="39f18-1535">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1536">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1536">Az.Compute</span></span>
* <span data-ttu-id="39f18-1537">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="39f18-1537">Proximity placement group feature.</span></span>
    - <span data-ttu-id="39f18-1538">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-1538">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="39f18-1539">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1539">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="39f18-1540">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="39f18-1540">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="39f18-1541">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="39f18-1541">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="39f18-1542">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-1542">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="39f18-1543">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="39f18-1543">Breaking changes</span></span>
    - <span data-ttu-id="39f18-1544">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="39f18-1544">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="39f18-1545">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="39f18-1545">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="39f18-1546">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="39f18-1546">Az.DeploymentManager</span></span>
* <span data-ttu-id="39f18-1547">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="39f18-1547">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="39f18-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="39f18-1548">Az.Dns</span></span>
* <span data-ttu-id="39f18-1549">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="39f18-1549">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="39f18-1550">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="39f18-1550">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="39f18-1551">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="39f18-1551">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="39f18-1552">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-1552">Az.FrontDoor</span></span>
* <span data-ttu-id="39f18-1553">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1553">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="39f18-1554">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="39f18-1554">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="39f18-1555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-1555">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-1556">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-1556">Removed two cmdlets:</span></span>
    - <span data-ttu-id="39f18-1557">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39f18-1557">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="39f18-1558">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39f18-1558">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="39f18-1559">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="39f18-1559">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="39f18-1560">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="39f18-1560">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="39f18-1561">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="39f18-1561">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="39f18-1562">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1562">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-1563">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-1563">Az.Monitor</span></span>
* <span data-ttu-id="39f18-1564">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="39f18-1564">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="39f18-1565">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="39f18-1565">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="39f18-1566">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-1566">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="39f18-1567">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="39f18-1567">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="39f18-1568">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="39f18-1568">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="39f18-1569">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="39f18-1569">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="39f18-1570">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="39f18-1570">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="39f18-1571">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39f18-1571">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39f18-1572">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39f18-1572">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39f18-1573">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39f18-1573">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39f18-1574">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39f18-1574">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39f18-1575">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="39f18-1575">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="39f18-1576">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="39f18-1576">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="39f18-1577">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="39f18-1577">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1578">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1578">Az.Network</span></span>
* <span data-ttu-id="39f18-1579">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="39f18-1579">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="39f18-1580">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-1580">New cmdlets</span></span>
        - <span data-ttu-id="39f18-1581">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-1581">New-AzNatGateway</span></span>
        - <span data-ttu-id="39f18-1582">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-1582">Get-AzNatGateway</span></span>
        - <span data-ttu-id="39f18-1583">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-1583">Set-AzNatGateway</span></span>
        - <span data-ttu-id="39f18-1584">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-1584">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="39f18-1585">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="39f18-1585">Updated cmdlets</span></span>
        - <span data-ttu-id="39f18-1586">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="39f18-1586">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="39f18-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="39f18-1587">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="39f18-1588">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1588">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="39f18-1589">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1589">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="39f18-1590">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="39f18-1590">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-1591">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1591">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-1592">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="39f18-1592">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="39f18-1593">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="39f18-1593">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="39f18-1594">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="39f18-1594">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1595">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1595">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1596">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="39f18-1596">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="39f18-1597">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="39f18-1597">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="39f18-1598">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="39f18-1598">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="39f18-1599">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1599">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="39f18-1600">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="39f18-1600">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="39f18-1601">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="39f18-1601">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="39f18-1602">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="39f18-1602">Az.Relay</span></span>
* <span data-ttu-id="39f18-1603">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="39f18-1603">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39f18-1604">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39f18-1604">Az.ServiceBus</span></span>
* <span data-ttu-id="39f18-1605">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="39f18-1605">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1606">Az.Storage</span></span>
* <span data-ttu-id="39f18-1607">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="39f18-1607">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="39f18-1608">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="39f18-1608">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="39f18-1609">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="39f18-1609">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="39f18-1610">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1610">New-AzStorageAccount</span></span>
* <span data-ttu-id="39f18-1611">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="39f18-1611">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="39f18-1612">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1612">New-AzStorageAccount</span></span>
    - <span data-ttu-id="39f18-1613">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1613">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="39f18-1614">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1614">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1615">Az.Websites</span></span>
* <span data-ttu-id="39f18-1616">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1616">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="39f18-1617">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="39f18-1617">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="39f18-1618">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1618">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39f18-1619">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="39f18-1619">Highlights since the last major release</span></span>
* <span data-ttu-id="39f18-1620">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="39f18-1620">General availability of `Az` module</span></span>
* <span data-ttu-id="39f18-1621">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="39f18-1621">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="39f18-1622">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="39f18-1622">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="39f18-1623">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1623">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="39f18-1624">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39f18-1624">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39f18-1625">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1625">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="39f18-1626">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="39f18-1626">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-1627">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1627">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1628">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="39f18-1628">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="39f18-1629">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39f18-1629">Az.Batch</span></span>
* <span data-ttu-id="39f18-1630">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-1631">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-1631">Az.Cdn</span></span>
* <span data-ttu-id="39f18-1632">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-1634">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1634">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1635">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1635">Az.Compute</span></span>
* <span data-ttu-id="39f18-1636">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="39f18-1636">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="39f18-1637">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39f18-1638">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="39f18-1638">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1639">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1639">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1640">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="39f18-1640">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-1641">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-1641">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-1642">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39f18-1643">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39f18-1643">Az.EventGrid</span></span>
* <span data-ttu-id="39f18-1644">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="39f18-1644">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-1645">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1645">Az.EventHub</span></span>
* <span data-ttu-id="39f18-1646">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="39f18-1646">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="39f18-1647">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="39f18-1647">Az.HDInsight</span></span>
* <span data-ttu-id="39f18-1648">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-1649">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1649">Az.IotHub</span></span>
* <span data-ttu-id="39f18-1650">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-1651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-1651">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-1652">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39f18-1653">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="39f18-1653">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="39f18-1654">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="39f18-1654">Az.MachineLearning</span></span>
* <span data-ttu-id="39f18-1655">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1655">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="39f18-1656">Az.Media</span><span class="sxs-lookup"><span data-stu-id="39f18-1656">Az.Media</span></span>
* <span data-ttu-id="39f18-1657">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1657">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-1658">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-1658">Az.Monitor</span></span>
  * <span data-ttu-id="39f18-1659">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="39f18-1659">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="39f18-1660">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="39f18-1660">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="39f18-1661">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="39f18-1661">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="39f18-1662">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="39f18-1662">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="39f18-1663">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="39f18-1663">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="39f18-1664">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="39f18-1664">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="39f18-1665">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="39f18-1665">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1666">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1666">Az.Network</span></span>
* <span data-ttu-id="39f18-1667">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1667">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39f18-1668">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="39f18-1668">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="39f18-1669">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="39f18-1669">Az.NotificationHubs</span></span>
* <span data-ttu-id="39f18-1670">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1670">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-1671">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1671">Az.OperationalInsights</span></span>
* <span data-ttu-id="39f18-1672">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="39f18-1673">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="39f18-1673">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="39f18-1674">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1674">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1675">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1675">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1676">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39f18-1677">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1677">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="39f18-1678">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="39f18-1678">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="39f18-1679">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="39f18-1679">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39f18-1680">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39f18-1680">Az.RedisCache</span></span>
* <span data-ttu-id="39f18-1681">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1681">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1682">Az.Resources</span></span>
* <span data-ttu-id="39f18-1683">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="39f18-1683">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1684">Az.Sql</span></span>
* <span data-ttu-id="39f18-1685">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="39f18-1685">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="39f18-1686">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1686">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39f18-1687">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="39f18-1687">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="39f18-1688">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="39f18-1688">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="39f18-1689">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="39f18-1689">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="39f18-1690">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="39f18-1690">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="39f18-1691">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="39f18-1691">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1692">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1692">Az.Websites</span></span>
* <span data-ttu-id="39f18-1693">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="39f18-1693">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="39f18-1694">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="39f18-1694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="39f18-1695">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="39f18-1695">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="39f18-1696">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="39f18-1696">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="39f18-1697">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1697">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39f18-1698">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="39f18-1698">Highlights since the last major release</span></span>
* <span data-ttu-id="39f18-1699">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="39f18-1699">General availability of `Az` module</span></span>
* <span data-ttu-id="39f18-1700">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="39f18-1700">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="39f18-1701">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="39f18-1701">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="39f18-1702">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1702">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="39f18-1703">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39f18-1703">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39f18-1704">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1704">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="39f18-1705">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="39f18-1705">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="39f18-1706">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1706">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1707">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="39f18-1707">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="39f18-1708">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1708">Az.AnalysisServices</span></span>
* <span data-ttu-id="39f18-1709">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="39f18-1709">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="39f18-1710">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="39f18-1710">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1711">Az.Automation</span></span>
* <span data-ttu-id="39f18-1712">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="39f18-1712">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="39f18-1713">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="39f18-1713">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="39f18-1714">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1714">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1715">Az.Compute</span></span>
* <span data-ttu-id="39f18-1716">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-1716">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="39f18-1717">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="39f18-1717">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="39f18-1718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-1718">Az.ContainerInstance</span></span>
* <span data-ttu-id="39f18-1719">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="39f18-1719">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1720">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1720">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1721">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="39f18-1721">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="39f18-1722">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="39f18-1722">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1723">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1723">Az.Resources</span></span>
* <span data-ttu-id="39f18-1724">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="39f18-1724">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="39f18-1725">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="39f18-1725">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="39f18-1726">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="39f18-1726">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="39f18-1727">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="39f18-1727">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="39f18-1728">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="39f18-1728">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="39f18-1729">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="39f18-1729">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1730">Az.Sql</span></span>
* <span data-ttu-id="39f18-1731">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="39f18-1731">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1732">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1732">Az.Storage</span></span>
* <span data-ttu-id="39f18-1733">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="39f18-1733">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="39f18-1734">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="39f18-1734">New-AzStorageContext</span></span>
* <span data-ttu-id="39f18-1735">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="39f18-1735">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="39f18-1736">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="39f18-1736">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="39f18-1737">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="39f18-1737">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="39f18-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1738">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="39f18-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1739">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="39f18-1740">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="39f18-1740">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="39f18-1741">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1741">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="39f18-1742">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1742">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="39f18-1743">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1743">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="39f18-1744">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="39f18-1744">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="39f18-1745">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1745">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="39f18-1746">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="39f18-1746">Highlights since the last major release</span></span>
* <span data-ttu-id="39f18-1747">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="39f18-1747">General availability of `Az` module</span></span>
* <span data-ttu-id="39f18-1748">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="39f18-1748">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="39f18-1749">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="39f18-1749">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="39f18-1750">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1750">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="39f18-1751">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39f18-1751">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39f18-1752">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1752">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="39f18-1753">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="39f18-1753">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1754">Az.Automation</span></span>
* <span data-ttu-id="39f18-1755">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="39f18-1755">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="39f18-1756">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="39f18-1756">Dynamic grouping</span></span>
    * <span data-ttu-id="39f18-1757">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="39f18-1757">Pre-Post script</span></span>
    * <span data-ttu-id="39f18-1758">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="39f18-1758">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1759">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1759">Az.Compute</span></span>
* <span data-ttu-id="39f18-1760">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="39f18-1760">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="39f18-1761">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="39f18-1761">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-1762">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-1762">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-1763">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-1763">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1764">Az.Network</span></span>
* <span data-ttu-id="39f18-1765">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1765">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="39f18-1766">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="39f18-1766">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1767">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1767">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1768">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="39f18-1768">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="39f18-1769">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="39f18-1769">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1770">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1770">Az.Resources</span></span>
* <span data-ttu-id="39f18-1771">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-1771">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="39f18-1772">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="39f18-1772">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1773">Az.Sql</span></span>
* <span data-ttu-id="39f18-1774">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="39f18-1774">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1775">Az.Storage</span></span>
* <span data-ttu-id="39f18-1776">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1776">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="39f18-1777">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1777">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="39f18-1778">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1778">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="39f18-1779">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1779">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="39f18-1780">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="39f18-1780">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="39f18-1781">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="39f18-1781">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="39f18-1782">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="39f18-1782">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1783">Az.Websites</span></span>
* <span data-ttu-id="39f18-1784">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="39f18-1784">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="39f18-1785">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1785">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1786">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1787">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="39f18-1787">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="39f18-1788">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1788">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1789">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1789">Az.Automation</span></span>
* <span data-ttu-id="39f18-1790">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1790">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="39f18-1791">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="39f18-1791">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="39f18-1792">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="39f18-1792">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-1793">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-1793">Az.Cdn</span></span>
* <span data-ttu-id="39f18-1794">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="39f18-1794">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1795">Az.Compute</span></span>
* <span data-ttu-id="39f18-1796">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="39f18-1796">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1797">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1797">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1798">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="39f18-1798">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39f18-1799">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1799">Az.LogicApp</span></span>
* <span data-ttu-id="39f18-1800">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="39f18-1800">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1801">Az.Network</span></span>
* <span data-ttu-id="39f18-1802">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1802">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1803">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1803">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1804">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-1804">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="39f18-1805">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="39f18-1805">SDK Update</span></span>
* <span data-ttu-id="39f18-1806">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="39f18-1806">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="39f18-1807">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="39f18-1807">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1808">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1808">Az.Resources</span></span>
* <span data-ttu-id="39f18-1809">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="39f18-1809">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="39f18-1810">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="39f18-1810">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="39f18-1811">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="39f18-1811">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="39f18-1812">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="39f18-1812">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="39f18-1813">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="39f18-1813">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="39f18-1814">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="39f18-1814">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1815">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1815">Az.Sql</span></span>
* <span data-ttu-id="39f18-1816">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="39f18-1816">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="39f18-1817">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="39f18-1817">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1818">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1818">Az.Storage</span></span>
* <span data-ttu-id="39f18-1819">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-1819">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="39f18-1820">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1820">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="39f18-1821">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1821">Az.AnalysisServices</span></span>
* <span data-ttu-id="39f18-1822">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="39f18-1822">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1823">Az.Automation</span></span>
* <span data-ttu-id="39f18-1824">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1824">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="39f18-1825">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1825">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="39f18-1826">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1826">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-1827">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1827">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-1828">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="39f18-1828">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1829">Az.Compute</span></span>
* <span data-ttu-id="39f18-1830">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="39f18-1830">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="39f18-1831">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="39f18-1831">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="39f18-1832">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="39f18-1832">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="39f18-1833">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="39f18-1833">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-1834">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-1834">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-1835">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="39f18-1835">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="39f18-1836">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1836">Az.EventHub</span></span>
* <span data-ttu-id="39f18-1837">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="39f18-1837">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-1838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-1838">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-1839">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="39f18-1839">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39f18-1840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1840">Az.LogicApp</span></span>
* <span data-ttu-id="39f18-1841">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1841">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="39f18-1842">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="39f18-1842">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="39f18-1843">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1843">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="39f18-1844">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39f18-1844">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="39f18-1845">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39f18-1845">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="39f18-1846">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39f18-1846">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="39f18-1847">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="39f18-1847">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="39f18-1848">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1848">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="39f18-1849">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1849">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="39f18-1850">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1850">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="39f18-1851">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1851">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="39f18-1852">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-1852">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="39f18-1853">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="39f18-1853">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="39f18-1854">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-1854">Az.Monitor</span></span>
* <span data-ttu-id="39f18-1855">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="39f18-1855">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1856">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1856">Az.Network</span></span>
* <span data-ttu-id="39f18-1857">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="39f18-1857">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-1858">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-1858">Az.OperationalInsights</span></span>
* <span data-ttu-id="39f18-1859">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="39f18-1859">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="39f18-1860">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="39f18-1860">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="39f18-1861">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="39f18-1861">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1862">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1862">Az.Resources</span></span>
* <span data-ttu-id="39f18-1863">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="39f18-1863">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="39f18-1864">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="39f18-1864">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="39f18-1865">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="39f18-1865">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="39f18-1866">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="39f18-1866">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1867">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1867">Az.Sql</span></span>
* <span data-ttu-id="39f18-1868">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="39f18-1868">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="39f18-1869">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="39f18-1869">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1870">Az.Websites</span></span>
* <span data-ttu-id="39f18-1871">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="39f18-1871">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="39f18-1872">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1872">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1873">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1873">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1874">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39f18-1874">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="39f18-1875">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1875">Az.AnalysisServices</span></span>
<span data-ttu-id="39f18-1876">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="39f18-1876">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1877">Az.Compute</span></span>
* <span data-ttu-id="39f18-1878">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="39f18-1878">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="39f18-1879">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="39f18-1879">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="39f18-1880">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="39f18-1880">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1881">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1881">Az.RecoveryServices</span></span>
<span data-ttu-id="39f18-1882">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="39f18-1882">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1883">Az.Resources</span></span>
* <span data-ttu-id="39f18-1884">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="39f18-1884">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="39f18-1885">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="39f18-1885">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="39f18-1886">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="39f18-1886">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="39f18-1887">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="39f18-1887">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1888">Az.Sql</span></span>
* <span data-ttu-id="39f18-1889">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f18-1889">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="39f18-1890">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="39f18-1890">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="39f18-1891">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="39f18-1891">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="39f18-1892">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1892">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1893">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1893">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1894">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1894">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="39f18-1895">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1895">Az.AnalysisServices</span></span>
* <span data-ttu-id="39f18-1896">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1896">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-1897">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-1897">Az.RecoveryServices</span></span>
* <span data-ttu-id="39f18-1898">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="39f18-1898">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="39f18-1899">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1899">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1900">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1901">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="39f18-1901">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="39f18-1902">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1902">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39f18-1903">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="39f18-1903">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="39f18-1904">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="39f18-1904">Az.Aks</span></span>
* <span data-ttu-id="39f18-1905">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1905">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="39f18-1906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-1906">Az.Automation</span></span>
* <span data-ttu-id="39f18-1907">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="39f18-1907">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="39f18-1908">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1908">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="39f18-1909">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="39f18-1909">Az.Cdn</span></span>
* <span data-ttu-id="39f18-1910">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1910">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1911">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1911">Az.Compute</span></span>
* <span data-ttu-id="39f18-1912">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="39f18-1912">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="39f18-1913">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="39f18-1913">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="39f18-1914">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="39f18-1914">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="39f18-1915">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="39f18-1915">Az.ContainerRegistry</span></span>
* <span data-ttu-id="39f18-1916">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1916">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="39f18-1917">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="39f18-1917">Az.DataFactory</span></span>
* <span data-ttu-id="39f18-1918">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="39f18-1918">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-1920">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="39f18-1920">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="39f18-1921">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="39f18-1921">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="39f18-1922">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1922">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-1923">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1923">Az.IotHub</span></span>
* <span data-ttu-id="39f18-1924">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="39f18-1924">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="39f18-1925">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-1925">Az.KeyVault</span></span>
* <span data-ttu-id="39f18-1926">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1926">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-1927">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-1927">Az.Network</span></span>
* <span data-ttu-id="39f18-1928">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1928">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1929">Az.Resources</span></span>
* <span data-ttu-id="39f18-1930">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="39f18-1930">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="39f18-1931">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="39f18-1931">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="39f18-1932">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="39f18-1932">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="39f18-1933">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="39f18-1933">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="39f18-1934">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="39f18-1934">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="39f18-1935">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="39f18-1935">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="39f18-1936">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="39f18-1936">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-1937">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-1937">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-1938">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="39f18-1938">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="39f18-1939">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="39f18-1939">Fix some error messages.</span></span>
* <span data-ttu-id="39f18-1940">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="39f18-1940">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="39f18-1941">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="39f18-1941">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="39f18-1942">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="39f18-1942">Az.SignalR</span></span>
* <span data-ttu-id="39f18-1943">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1943">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1944">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1944">Az.Sql</span></span>
* <span data-ttu-id="39f18-1945">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1945">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39f18-1946">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="39f18-1946">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="39f18-1947">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="39f18-1947">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="39f18-1948">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="39f18-1948">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1949">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1949">Az.Storage</span></span>
* <span data-ttu-id="39f18-1950">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1950">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39f18-1951">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="39f18-1951">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="39f18-1952">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="39f18-1952">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="39f18-1953">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="39f18-1953">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="39f18-1954">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="39f18-1954">Az.TrafficManager</span></span>
* <span data-ttu-id="39f18-1955">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1955">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-1956">Az.Websites</span></span>
* <span data-ttu-id="39f18-1957">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="39f18-1957">Update incorrect online help URLs</span></span>
* <span data-ttu-id="39f18-1958">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-1958">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="39f18-1959">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="39f18-1959">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="39f18-1960">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="39f18-1960">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="39f18-1961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1961">Az.Accounts</span></span>
* <span data-ttu-id="39f18-1962">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="39f18-1962">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-1963">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-1963">Az.Compute</span></span>
* <span data-ttu-id="39f18-1964">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="39f18-1964">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="39f18-1965">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="39f18-1965">Updated the description of ID in help files</span></span>
* <span data-ttu-id="39f18-1966">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1966">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-1967">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-1967">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-1968">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="39f18-1968">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="39f18-1969">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="39f18-1969">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="39f18-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="39f18-1970">Az.EventGrid</span></span>
* <span data-ttu-id="39f18-1971">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="39f18-1971">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="39f18-1972">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="39f18-1972">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="39f18-1973">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="39f18-1973">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="39f18-1974">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="39f18-1974">Event Time-To-Live,</span></span>
        - <span data-ttu-id="39f18-1975">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="39f18-1975">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="39f18-1976">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="39f18-1976">Dead letter endpoint.</span></span>
    - <span data-ttu-id="39f18-1977">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="39f18-1977">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="39f18-1978">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="39f18-1978">Event Time-To-Live,</span></span>
        - <span data-ttu-id="39f18-1979">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="39f18-1979">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="39f18-1980">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="39f18-1980">Dead letter endpoint.</span></span>
* <span data-ttu-id="39f18-1981">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="39f18-1981">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="39f18-1982">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="39f18-1982">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="39f18-1983">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1983">Az.IotHub</span></span>
* <span data-ttu-id="39f18-1984">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="39f18-1984">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="39f18-1985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="39f18-1985">Az.LogicApp</span></span>
* <span data-ttu-id="39f18-1986">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="39f18-1986">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-1987">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-1987">Az.Resources</span></span>
* <span data-ttu-id="39f18-1988">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="39f18-1988">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="39f18-1989">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="39f18-1989">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="39f18-1990">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="39f18-1990">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="39f18-1991">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="39f18-1991">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="39f18-1992">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="39f18-1992">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="39f18-1993">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="39f18-1993">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="39f18-1994">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="39f18-1994">Az.SignalR</span></span>
* <span data-ttu-id="39f18-1995">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-1995">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-1996">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-1996">Az.Sql</span></span>
* <span data-ttu-id="39f18-1997">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="39f18-1997">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="39f18-1998">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-1998">Az.Storage</span></span>
* <span data-ttu-id="39f18-1999">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="39f18-1999">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="39f18-2000">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="39f18-2000">New-AzStorageContext</span></span>
* <span data-ttu-id="39f18-2001">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="39f18-2001">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="39f18-2002">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="39f18-2002">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-2003">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-2003">Az.Websites</span></span>
* <span data-ttu-id="39f18-2004">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="39f18-2004">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="39f18-2005">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-2005">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="39f18-2006">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2006">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="39f18-2007">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-2007">General</span></span>

- <span data-ttu-id="39f18-2008">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="39f18-2008">General Availability of Az Module</span></span>
- <span data-ttu-id="39f18-2009">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="39f18-2009">Online help for each module</span></span>
- <span data-ttu-id="39f18-2010">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="39f18-2010">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="39f18-2011">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="39f18-2011">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="39f18-2012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-2012">Az.Accounts</span></span>
- <span data-ttu-id="39f18-2013">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39f18-2013">Changed from Az.Profile</span></span>
- <span data-ttu-id="39f18-2014">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="39f18-2014">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="39f18-2015">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-2015">Az.ApiManagement</span></span>
- <span data-ttu-id="39f18-2016">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="39f18-2016">Fixes for #7002</span></span>
- <span data-ttu-id="39f18-2017">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2017">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="39f18-2018">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="39f18-2018">Az.Batch</span></span>
- <span data-ttu-id="39f18-2019">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="39f18-2019">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="39f18-2020">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="39f18-2020">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="39f18-2021">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="39f18-2022">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="39f18-2022">Az.Billing</span></span>
- <span data-ttu-id="39f18-2023">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2023">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="39f18-2024">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="39f18-2024">Az.CognitivServices</span></span>
- <span data-ttu-id="39f18-2025">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-2025">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="39f18-2026">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="39f18-2026">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="39f18-2027">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-2027">Az.ContainerInstance</span></span>
- <span data-ttu-id="39f18-2028">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="39f18-2028">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="39f18-2029">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="39f18-2029">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="39f18-2030">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2030">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="39f18-2031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-2031">Az.DataLakeStore</span></span>
- <span data-ttu-id="39f18-2032">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2032">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="39f18-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="39f18-2033">Az.Monitor</span></span>
- <span data-ttu-id="39f18-2034">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2034">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="39f18-2035">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="39f18-2035">Az.KeyVault</span></span>
- <span data-ttu-id="39f18-2036">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="39f18-2036">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="39f18-2037">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="39f18-2037">Az.MachineLearning</span></span>
- <span data-ttu-id="39f18-2038">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="39f18-2038">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="39f18-2039">Az.Media</span><span class="sxs-lookup"><span data-stu-id="39f18-2039">Az.Media</span></span>
- <span data-ttu-id="39f18-2040">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="39f18-2040">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="39f18-2041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-2041">Az.Network</span></span>
<span data-ttu-id="39f18-2042">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="39f18-2042">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="39f18-2043">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="39f18-2043">New cmdlets added:</span></span>
        - <span data-ttu-id="39f18-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2044">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39f18-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2045">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39f18-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2046">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39f18-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2047">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39f18-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2048">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="39f18-2049">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="39f18-2049">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="39f18-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2050">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="39f18-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="39f18-2051">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="39f18-2052">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="39f18-2052">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="39f18-2053">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39f18-2053">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="39f18-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="39f18-2054">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="39f18-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="39f18-2055">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="39f18-2056">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-2056">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="39f18-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-2057">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="39f18-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="39f18-2058">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="39f18-2059">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="39f18-2059">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="39f18-2060">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39f18-2060">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="39f18-2061">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39f18-2061">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="39f18-2062">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="39f18-2062">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="39f18-2063">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="39f18-2063">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="39f18-2064">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2064">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="39f18-2065">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-2065">Az.OperationalInsights</span></span>
- <span data-ttu-id="39f18-2066">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2066">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="39f18-2067">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39f18-2067">Az.Profile</span></span>
- <span data-ttu-id="39f18-2068">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="39f18-2068">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-2069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-2069">Az.RecoveryServices</span></span>
- <span data-ttu-id="39f18-2070">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2070">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="39f18-2071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-2071">Az.Resources</span></span>
- <span data-ttu-id="39f18-2072">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2072">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="39f18-2073">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-2073">Az.ServiceFabric</span></span>
- <span data-ttu-id="39f18-2074">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="39f18-2074">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="39f18-2075">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2075">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="39f18-2076">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="39f18-2076">Az.SIgnalR</span></span>
- <span data-ttu-id="39f18-2077">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="39f18-2077">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="39f18-2078">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-2078">Az.Sql</span></span>
- <span data-ttu-id="39f18-2079">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="39f18-2079">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="39f18-2080">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-2080">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="39f18-2081">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="39f18-2082">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-2082">Az.Storage</span></span>
- <span data-ttu-id="39f18-2083">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2083">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="39f18-2084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-2084">Az.Websites</span></span>
- <span data-ttu-id="39f18-2085">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="39f18-2085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="39f18-2086">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2086">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="39f18-2087">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-2087">General</span></span>

* <span data-ttu-id="39f18-2088">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="39f18-2088">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="39f18-2089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-2089">Az.Compute</span></span>

* <span data-ttu-id="39f18-2090">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="39f18-2090">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="39f18-2091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-2091">Az.DataLakeStore</span></span>

* <span data-ttu-id="39f18-2092">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="39f18-2092">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="39f18-2093">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="39f18-2093">Az.FrontDoor</span></span>

* <span data-ttu-id="39f18-2094">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="39f18-2094">Fixed some broken links</span></span>
    - <span data-ttu-id="39f18-2095">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="39f18-2095">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="39f18-2096">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="39f18-2096">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="39f18-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="39f18-2097">Az.RecoveryServices</span></span>

* <span data-ttu-id="39f18-2098">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-2098">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="39f18-2099">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="39f18-2099">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="39f18-2100">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-2100">Az.Resources</span></span>

* <span data-ttu-id="39f18-2101">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="39f18-2101">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="39f18-2102">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="39f18-2102">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="39f18-2103">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-2103">Az.Sql</span></span>

* <span data-ttu-id="39f18-2104">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="39f18-2104">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="39f18-2105">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="39f18-2105">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="39f18-2106">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="39f18-2106">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="39f18-2107">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-2107">Az.Storage</span></span>

* <span data-ttu-id="39f18-2108">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-2108">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="39f18-2109">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="39f18-2109">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="39f18-2110">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="39f18-2110">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="39f18-2111">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="39f18-2111">Support Static Website configuration</span></span>
    - <span data-ttu-id="39f18-2112">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="39f18-2112">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="39f18-2113">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="39f18-2113">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="39f18-2114">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-2114">Az.Websites</span></span>

* <span data-ttu-id="39f18-2115">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="39f18-2115">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="39f18-2116">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="39f18-2116">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="39f18-2117">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="39f18-2117">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="39f18-2118">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2118">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="39f18-2119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="39f18-2119">Az.ApiManagement</span></span>
* <span data-ttu-id="39f18-2120">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="39f18-2120">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="39f18-2121">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="39f18-2121">Az.Automation</span></span>
* <span data-ttu-id="39f18-2122">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="39f18-2122">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="39f18-2123">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="39f18-2123">Added Update Management cmdlets</span></span>
* <span data-ttu-id="39f18-2124">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="39f18-2124">Added Source Control cmdlets</span></span>
* <span data-ttu-id="39f18-2125">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="39f18-2125">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="39f18-2126">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="39f18-2126">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="39f18-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-2127">Az.Compute</span></span>
* <span data-ttu-id="39f18-2128">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="39f18-2128">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="39f18-2129">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="39f18-2129">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="39f18-2130">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-2130">Az.ContainerInstance</span></span>
* <span data-ttu-id="39f18-2131">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="39f18-2131">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="39f18-2132">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="39f18-2132">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="39f18-2133">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="39f18-2133">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="39f18-2134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-2134">Az.Network</span></span>
* <span data-ttu-id="39f18-2135">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="39f18-2135">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="39f18-2136">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="39f18-2136">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="39f18-2137">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39f18-2137">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="39f18-2138">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="39f18-2138">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="39f18-2139">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="39f18-2139">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="39f18-2140">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="39f18-2140">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="39f18-2141">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="39f18-2141">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="39f18-2142">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="39f18-2142">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="39f18-2143">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="39f18-2143">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="39f18-2144">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="39f18-2144">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="39f18-2145">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="39f18-2145">Az.Relay</span></span>
* <span data-ttu-id="39f18-2146">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="39f18-2146">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="39f18-2147">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-2147">Az.Resources</span></span>
* <span data-ttu-id="39f18-2148">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="39f18-2148">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="39f18-2149">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="39f18-2149">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="39f18-2150">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="39f18-2150">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="39f18-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-2152">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="39f18-2152">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="39f18-2153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-2153">Az.Sql</span></span>
* <span data-ttu-id="39f18-2154">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="39f18-2154">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="39f18-2155">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-2155">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39f18-2156">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-2156">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39f18-2157">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-2157">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39f18-2158">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="39f18-2158">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="39f18-2159">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39f18-2159">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="39f18-2160">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39f18-2160">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="39f18-2161">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39f18-2161">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="39f18-2162">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="39f18-2162">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="39f18-2163">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="39f18-2163">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="39f18-2164">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="39f18-2164">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="39f18-2165">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="39f18-2165">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="39f18-2166">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="39f18-2166">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="39f18-2167">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="39f18-2167">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="39f18-2168">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="39f18-2168">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="39f18-2169">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="39f18-2169">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="39f18-2170">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="39f18-2170">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="39f18-2171">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2171">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="39f18-2172">Generale</span><span class="sxs-lookup"><span data-stu-id="39f18-2172">General</span></span>
* <span data-ttu-id="39f18-2173">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="39f18-2173">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="39f18-2174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39f18-2174">Az.Profile</span></span>
* <span data-ttu-id="39f18-2175">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39f18-2175">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="39f18-2176">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="39f18-2176">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="39f18-2177">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="39f18-2177">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="39f18-2178">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="39f18-2178">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="39f18-2179">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="39f18-2179">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="39f18-2180">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="39f18-2180">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="39f18-2181">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="39f18-2181">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-2182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-2182">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-2183">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="39f18-2183">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-2184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-2184">Az.Compute</span></span>
* <span data-ttu-id="39f18-2185">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="39f18-2185">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="39f18-2186">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="39f18-2186">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="39f18-2187">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="39f18-2187">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-2188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-2188">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-2189">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="39f18-2189">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="39f18-2190">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="39f18-2190">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="39f18-2191">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="39f18-2191">Az.Insights</span></span>
* <span data-ttu-id="39f18-2192">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="39f18-2192">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="39f18-2193">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="39f18-2193">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="39f18-2194">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="39f18-2194">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="39f18-2195">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="39f18-2195">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-2196">Az.Network</span></span>
* <span data-ttu-id="39f18-2197">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="39f18-2197">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="39f18-2198">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="39f18-2198">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="39f18-2199">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="39f18-2199">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="39f18-2200">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="39f18-2200">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="39f18-2201">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="39f18-2201">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="39f18-2202">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="39f18-2202">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="39f18-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="39f18-2203">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="39f18-2204">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="39f18-2204">Az.PolicyInsights</span></span>
* <span data-ttu-id="39f18-2205">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="39f18-2205">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-2206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-2206">Az.Resources</span></span>
* <span data-ttu-id="39f18-2207">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="39f18-2207">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="39f18-2208">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="39f18-2208">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="39f18-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39f18-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="39f18-2210">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="39f18-2210">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="39f18-2211">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="39f18-2211">Az.ServiceFabric</span></span>
* <span data-ttu-id="39f18-2212">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="39f18-2212">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="39f18-2213">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="39f18-2213">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="39f18-2214">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="39f18-2214">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="39f18-2215">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="39f18-2215">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="39f18-2216">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="39f18-2216">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="39f18-2217">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2217">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="39f18-2218">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="39f18-2218">Az.Profile</span></span>
* <span data-ttu-id="39f18-2219">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="39f18-2219">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="39f18-2220">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="39f18-2220">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-2221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-2221">Az.Compute</span></span>
* <span data-ttu-id="39f18-2222">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="39f18-2222">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="39f18-2223">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f18-2223">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="39f18-2224">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="39f18-2224">Az.DataLakeStore</span></span>
* <span data-ttu-id="39f18-2225">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="39f18-2225">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="39f18-2226">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39f18-2226">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="39f18-2227">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="39f18-2227">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="39f18-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="39f18-2228">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="39f18-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39f18-2229">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-2230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-2230">Az.Network</span></span>
* <span data-ttu-id="39f18-2231">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="39f18-2231">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="39f18-2232">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f18-2232">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-2233">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-2233">Az.Resources</span></span>
* <span data-ttu-id="39f18-2234">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="39f18-2234">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="39f18-2235">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="39f18-2235">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="39f18-2236">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2236">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="39f18-2237">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="39f18-2237">Azure.Storage</span></span>
* <span data-ttu-id="39f18-2238">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="39f18-2238">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="39f18-2239">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="39f18-2239">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="39f18-2240">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="39f18-2240">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="39f18-2241">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="39f18-2241">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="39f18-2242">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="39f18-2242">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="39f18-2243">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="39f18-2243">Az.CognitiveServices</span></span>
* <span data-ttu-id="39f18-2244">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="39f18-2244">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="39f18-2245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="39f18-2245">Az.Compute</span></span>
* <span data-ttu-id="39f18-2246">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="39f18-2246">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="39f18-2247">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="39f18-2247">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="39f18-2248">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="39f18-2248">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="39f18-2249">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="39f18-2249">Az.DataFactoryV2</span></span>
* <span data-ttu-id="39f18-2250">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="39f18-2250">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="39f18-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="39f18-2251">Az.Network</span></span>
* <span data-ttu-id="39f18-2252">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39f18-2252">Added NetworkProfile functionality.</span></span> <span data-ttu-id="39f18-2253">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="39f18-2253">new cmdlets added</span></span>
    - <span data-ttu-id="39f18-2254">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39f18-2254">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="39f18-2255">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39f18-2255">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="39f18-2256">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39f18-2256">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="39f18-2257">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="39f18-2257">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="39f18-2258">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-2258">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="39f18-2259">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-2259">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="39f18-2260">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="39f18-2260">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="39f18-2261">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="39f18-2261">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="39f18-2262">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="39f18-2262">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="39f18-2263">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="39f18-2263">Az.RedisCache</span></span>
* <span data-ttu-id="39f18-2264">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="39f18-2264">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="39f18-2265">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="39f18-2265">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="39f18-2266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="39f18-2266">Az.Resources</span></span>
* <span data-ttu-id="39f18-2267">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="39f18-2267">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="39f18-2268">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="39f18-2268">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="39f18-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="39f18-2269">Az.Sql</span></span>
* <span data-ttu-id="39f18-2270">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="39f18-2270">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="39f18-2271">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="39f18-2271">Az.Websites</span></span>
* <span data-ttu-id="39f18-2272">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="39f18-2272">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="39f18-2273">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="39f18-2273">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="39f18-2274">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="39f18-2274">0.2.0 - September 2018</span></span>
 <span data-ttu-id="39f18-2275">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="39f18-2275">Initial Release</span></span>
