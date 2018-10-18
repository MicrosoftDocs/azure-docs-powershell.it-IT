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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399060"
---
# <a name="release-notes"></a><span data-ttu-id="2667d-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="2667d-103">Release notes</span></span>

<span data-ttu-id="2667d-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="2667d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="2667d-105">6.10.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2667d-106">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-106">Azure.Storage</span></span>
* <span data-ttu-id="2667d-107">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="2667d-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2667d-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2667d-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2667d-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2667d-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="2667d-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2667d-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="2667d-111">Supporto di Get-AzureRmCognitiveServicesAccountSkus senza un account esistente</span><span class="sxs-lookup"><span data-stu-id="2667d-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-112">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-113">Correzione di Get-AzureRmVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="2667d-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2667d-114">Aggiunta di un esempio di SimpleParameterSet alla Guida del cmdlet New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="2667d-115">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="2667d-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2667d-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2667d-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2667d-117">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="2667d-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-118">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-119">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2667d-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2667d-120">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2667d-120">new cmdlets added</span></span>
    - <span data-ttu-id="2667d-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2667d-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="2667d-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2667d-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="2667d-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2667d-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="2667d-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2667d-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="2667d-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="2667d-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2667d-127">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="2667d-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2667d-128">Aggiunta dei cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap e Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2667d-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="2667d-129">Aggiunta dei cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig e Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="2667d-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2667d-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="2667d-131">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="2667d-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2667d-132">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2667d-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-133">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-134">Aggiunta del parametro -Mode mancante a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2667d-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="2667d-135">Correzione del bug del cmdlet Get-AzureRmProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="2667d-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2667d-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-136">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-137">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="2667d-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2667d-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-138">AzureRM.Storage</span></span>
* <span data-ttu-id="2667d-139">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="2667d-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2667d-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2667d-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-141">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-142">Nuovo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="2667d-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2667d-143">Nuovi cmdlet New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="2667d-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="2667d-144">6.9.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2667d-145">Generale</span><span class="sxs-lookup"><span data-stu-id="2667d-145">General</span></span>
* <span data-ttu-id="2667d-146">Aggiunta di AzureRM.SignalR al modulo di rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="2667d-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2667d-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-147">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-148">Modifiche minori al codice comune di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2667d-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="2667d-149">Aggiornamento dei file della Guida per includere tipi di parametri completi.</span><span class="sxs-lookup"><span data-stu-id="2667d-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="2667d-150">Modifica di -ServicePrincipal in non obbligatorio nel set di parametri ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2667d-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="2667d-151">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-151">Azure.Storage</span></span>
* <span data-ttu-id="2667d-152">Supporto della creazione del contesto di archiviazione con OAuth.</span><span class="sxs-lookup"><span data-stu-id="2667d-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="2667d-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2667d-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="2667d-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="2667d-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="2667d-155">Aggiunta di Standard_Microsoft nello SKU del piano tariffario per la rete CDN.</span><span class="sxs-lookup"><span data-stu-id="2667d-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-156">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-157">Trasferimento delle dipendenze da Key Vault e Archiviazione a dipendenze comuni</span><span class="sxs-lookup"><span data-stu-id="2667d-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="2667d-158">Aggiunta del supporto per altre dimensioni delle macchine virtuali ai cmdlet AEM</span><span class="sxs-lookup"><span data-stu-id="2667d-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="2667d-159">Aggiunta del parametro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="2667d-160">Aggiunta del parametro ResourceId a Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="2667d-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="2667d-161">Aggiunta del cmdlet Invoke-AzureRmVmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2667d-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="2667d-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="2667d-162">AzureRM.Dns</span></span>
* <span data-ttu-id="2667d-163">Aggiunta del supporto per record alias durante la creazione del record DNS</span><span class="sxs-lookup"><span data-stu-id="2667d-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2667d-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2667d-164">AzureRM.Insights</span></span>
* <span data-ttu-id="2667d-165">Risoluzione dei problemi 6833 e 7102 (area Impostazioni di diagnostica)</span><span class="sxs-lookup"><span data-stu-id="2667d-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="2667d-166">Problemi con il nome predefinito, ovvero 'service', durante la creazione e l'elencazione/ottenimento delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="2667d-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="2667d-167">Problemi nella creazione di impostazioni di diagnostica con categorie</span><span class="sxs-lookup"><span data-stu-id="2667d-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="2667d-168">Aggiunta del messaggio di funzione deprecata per i parametri degli intervalli di tempo delle metriche</span><span class="sxs-lookup"><span data-stu-id="2667d-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="2667d-169">I parametri timegrains vengono ancora accettati (si tratta di una modifica che non causa interruzioni), ma vengono ignorati nel back-end perché solo PT1M è valido</span><span class="sxs-lookup"><span data-stu-id="2667d-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-170">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-171">Modifiche ai cmdlet LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2667d-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="2667d-172">LoadBalancerInboundNatPoolConfig: aggiunta dei parametri IdleTimeoutInMinutes, EnableFloatingIp ed EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2667d-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="2667d-173">LoadBalancerInboundNatRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2667d-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="2667d-174">LoadBalancerRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2667d-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="2667d-175">LoadBalancerProbeConfig: aggiunta del supporto del valore "Https" per il parametro Protocol</span><span class="sxs-lookup"><span data-stu-id="2667d-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="2667d-176">Aggiunta di nuovi comandi per la nuova OutboundRule delle sottorisorse di LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2667d-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="2667d-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="2667d-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="2667d-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="2667d-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="2667d-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="2667d-182">Aggiunta della nuova proprietà HostedWorkloads per PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2667d-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="2667d-183">Aggiunta di nuovi cmdlet per la funzionalità Firewall di Azure tramite ARM</span><span class="sxs-lookup"><span data-stu-id="2667d-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="2667d-184">Aggiunta di Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2667d-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="2667d-185">Aggiunta di Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2667d-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="2667d-186">Aggiunta di New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2667d-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="2667d-187">Aggiunta di Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2667d-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="2667d-188">Aggiunta di New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2667d-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="2667d-189">Aggiunta di New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="2667d-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="2667d-190">Aggiunta di New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2667d-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="2667d-191">Aggiunta di New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="2667d-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="2667d-192">Aggiunta di New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2667d-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="2667d-193">Aggiunta di New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2667d-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="2667d-194">Aggiunta del supporto per il certificato radice attendibile e la configurazione della scalabilità automatica nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2667d-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="2667d-195">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2667d-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="2667d-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="2667d-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="2667d-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="2667d-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="2667d-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="2667d-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="2667d-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="2667d-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="2667d-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="2667d-205">Aggiornamento dei cmdlet con il parametro facoltativo -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="2667d-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2667d-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="2667d-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2667d-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="2667d-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2667d-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="2667d-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2667d-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="2667d-210">Aggiornamento dei cmdlet con il parametro facoltativo -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="2667d-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2667d-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="2667d-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2667d-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="2667d-213">Aggiunta di un cmdlet per l'endpoint di interfaccia Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2667d-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="2667d-214">Aggiunta del supporto per più prefissi di indirizzi in una sottorete.</span><span class="sxs-lookup"><span data-stu-id="2667d-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="2667d-215">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2667d-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="2667d-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="2667d-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="2667d-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="2667d-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="2667d-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="2667d-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="2667d-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="2667d-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="2667d-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="2667d-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="2667d-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="2667d-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="2667d-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="2667d-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="2667d-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="2667d-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="2667d-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="2667d-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="2667d-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2667d-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="2667d-235">Aggiunta di cmdlet per la delega di subnet.</span><span class="sxs-lookup"><span data-stu-id="2667d-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="2667d-236">New-AzureRmDelegation: crea una nuova delega che può essere aggiunta a una subnet</span><span class="sxs-lookup"><span data-stu-id="2667d-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="2667d-237">Remove-AzureRmDelegation: acquisisce una subnet e rimuove il nome di delega fornito da tale subnet</span><span class="sxs-lookup"><span data-stu-id="2667d-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="2667d-238">Add-AzureRmDelegation: acquisisce una subnet e aggiunge il nome servizio specificato come delega a tale subnet</span><span class="sxs-lookup"><span data-stu-id="2667d-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="2667d-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="2667d-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="2667d-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="2667d-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2667d-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2667d-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2667d-242">Supporto per dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="2667d-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="2667d-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2667d-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="2667d-244">Aggiornamento della dipendenza di Insights.</span><span class="sxs-lookup"><span data-stu-id="2667d-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-245">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-246">Aggiornamento di New-AzureRmResourceGroupDeployment con il nuovo parametro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="2667d-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="2667d-247">Aggiunta del supporto per OnErrorDeployment con il nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="2667d-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="2667d-248">Supporto dell'identità gestita per le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2667d-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="2667d-249">Non sono più necessari parametri con valori predefiniti durante l'assegnazione di criteri con 'New-AzureRmPolicyAssignment'</span><span class="sxs-lookup"><span data-stu-id="2667d-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="2667d-250">Aggiunta del nuovo cmdlet Get-AzureRmPolicyAlias per il recupero di alias dei criteri</span><span class="sxs-lookup"><span data-stu-id="2667d-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-252">Risoluzione del problema #7161</span><span class="sxs-lookup"><span data-stu-id="2667d-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="2667d-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="2667d-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="2667d-254">Aggiornamento dei nomi SKU in Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="2667d-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="2667d-255">Aggiunta del campo di versione all'oggetto PSSignalRResource e della stringa di connessione all'oggetto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="2667d-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2667d-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-256">AzureRM.Storage</span></span>
* <span data-ttu-id="2667d-257">Supporto dei criteri di immutabilità in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="2667d-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2667d-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="2667d-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2667d-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="2667d-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2667d-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="2667d-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2667d-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="2667d-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2667d-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="2667d-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="2667d-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="2667d-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="2667d-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="2667d-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="2667d-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="2667d-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="2667d-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-269">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-270">Aggiunta di due nuovi cmdlet: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="2667d-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="2667d-271">New-AzureRmAppServicePlan - Aggiunta dello switch HyperV per la creazione di un piano del servizio app con il contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="2667d-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="2667d-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Aggiunta di nuovi parametri (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) per la creazione e la gestione di app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="2667d-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="2667d-273">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2667d-274">Generale</span><span class="sxs-lookup"><span data-stu-id="2667d-274">General</span></span>
* <span data-ttu-id="2667d-275">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2667d-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="2667d-276">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="2667d-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2667d-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2667d-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2667d-278">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2667d-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="2667d-279">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="2667d-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="2667d-280">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="2667d-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="2667d-281">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="2667d-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="2667d-282">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2667d-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="2667d-283">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="2667d-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="2667d-284">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="2667d-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="2667d-285">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="2667d-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="2667d-286">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="2667d-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="2667d-287">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="2667d-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="2667d-288">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="2667d-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="2667d-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-289">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-290">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2667d-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="2667d-291">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="2667d-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="2667d-292">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2667d-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="2667d-293">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="2667d-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-294">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-295">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="2667d-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2667d-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2667d-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2667d-297">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="2667d-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="2667d-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-298">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-299">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2667d-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-301">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="2667d-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2667d-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2667d-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2667d-303">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2667d-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="2667d-304">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2667d-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="2667d-305">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="2667d-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="2667d-306">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2667d-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="2667d-307">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="2667d-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="2667d-308">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="2667d-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="2667d-309">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2667d-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="2667d-310">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2667d-311">Generale</span><span class="sxs-lookup"><span data-stu-id="2667d-311">General</span></span>
* <span data-ttu-id="2667d-312">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2667d-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2667d-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-313">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-314">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="2667d-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-315">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-316">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2667d-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="2667d-317">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="2667d-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="2667d-318">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="2667d-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="2667d-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="2667d-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="2667d-320">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="2667d-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-321">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-322">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="2667d-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2667d-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2667d-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2667d-324">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="2667d-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-325">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-326">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2667d-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-328">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="2667d-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2667d-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2667d-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2667d-330">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2667d-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="2667d-331">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2667d-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="2667d-332">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="2667d-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="2667d-333">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2667d-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="2667d-334">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="2667d-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="2667d-335">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="2667d-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="2667d-336">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2667d-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-337">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-338">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="2667d-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="2667d-339">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2667d-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-340">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-341">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2667d-342">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="2667d-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="2667d-343">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="2667d-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="2667d-344">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="2667d-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="2667d-345">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-345">Azure.Storage</span></span>
* <span data-ttu-id="2667d-346">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="2667d-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="2667d-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="2667d-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2667d-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2667d-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2667d-349">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="2667d-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2667d-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="2667d-351">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2667d-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2667d-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2667d-353">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="2667d-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2667d-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="2667d-355">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2667d-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2667d-356">AzureRM.Automation</span></span>
* <span data-ttu-id="2667d-357">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="2667d-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="2667d-358">AzureRM.Backup</span></span>
* <span data-ttu-id="2667d-359">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2667d-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2667d-360">AzureRM.Batch</span></span>
* <span data-ttu-id="2667d-361">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="2667d-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="2667d-362">AzureRM.Billing</span></span>
* <span data-ttu-id="2667d-363">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="2667d-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="2667d-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="2667d-365">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="2667d-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2667d-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="2667d-367">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-368">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-369">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2667d-370">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="2667d-371">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="2667d-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="2667d-372">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2667d-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2667d-373">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="2667d-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2667d-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2667d-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="2667d-375">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="2667d-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2667d-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="2667d-377">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="2667d-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2667d-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="2667d-379">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="2667d-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2667d-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="2667d-381">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2667d-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2667d-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2667d-383">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2667d-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2667d-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2667d-385">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2667d-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2667d-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2667d-387">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="2667d-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="2667d-388">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2667d-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="2667d-389">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2667d-390">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2667d-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="2667d-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2667d-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="2667d-392">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="2667d-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="2667d-393">AzureRM.Dns</span></span>
* <span data-ttu-id="2667d-394">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2667d-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2667d-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2667d-396">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2667d-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2667d-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="2667d-398">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="2667d-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2667d-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="2667d-400">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2667d-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2667d-401">AzureRM.Insights</span></span>
* <span data-ttu-id="2667d-402">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="2667d-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="2667d-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="2667d-404">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2667d-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2667d-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2667d-406">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2667d-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2667d-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2667d-408">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="2667d-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2667d-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="2667d-410">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="2667d-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2667d-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="2667d-412">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="2667d-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2667d-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="2667d-414">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="2667d-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="2667d-415">AzureRM.Media</span></span>
* <span data-ttu-id="2667d-416">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-417">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-418">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2667d-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="2667d-419">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2667d-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2667d-420">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2667d-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="2667d-421">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2667d-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="2667d-422">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2667d-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="2667d-423">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2667d-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2667d-424">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="2667d-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="2667d-425">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="2667d-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="2667d-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2667d-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="2667d-427">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="2667d-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2667d-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2667d-429">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2667d-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2667d-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2667d-431">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2667d-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2667d-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2667d-433">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="2667d-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2667d-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="2667d-435">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2667d-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2667d-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2667d-437">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="2667d-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="2667d-438">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="2667d-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="2667d-439">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="2667d-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="2667d-440">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2667d-441">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="2667d-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="2667d-442">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="2667d-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="2667d-443">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="2667d-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2667d-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2667d-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2667d-445">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="2667d-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2667d-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="2667d-447">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2667d-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2667d-448">AzureRM.Relay</span></span>
* <span data-ttu-id="2667d-449">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-450">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-451">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2667d-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="2667d-452">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2667d-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="2667d-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="2667d-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="2667d-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="2667d-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="2667d-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="2667d-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="2667d-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="2667d-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2667d-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="2667d-460">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="2667d-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="2667d-461">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="2667d-462">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2667d-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2667d-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2667d-464">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-466">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2667d-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2667d-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2667d-468">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2667d-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-469">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-470">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2667d-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-471">AzureRM.Storage</span></span>
* <span data-ttu-id="2667d-472">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="2667d-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="2667d-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="2667d-474">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="2667d-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2667d-475">AzureRM.Tags</span></span>
* <span data-ttu-id="2667d-476">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2667d-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2667d-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2667d-478">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="2667d-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="2667d-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="2667d-480">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-481">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-482">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2667d-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="2667d-483">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2667d-484">Generale</span><span class="sxs-lookup"><span data-stu-id="2667d-484">General</span></span>
* <span data-ttu-id="2667d-485">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="2667d-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2667d-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-486">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-487">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2667d-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="2667d-488">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2667d-489">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-489">Azure.Storage</span></span>
* <span data-ttu-id="2667d-490">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2667d-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="2667d-491">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2667d-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2667d-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2667d-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2667d-493">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="2667d-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="2667d-494">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="2667d-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="2667d-495">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="2667d-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="2667d-496">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="2667d-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="2667d-497">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="2667d-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="2667d-498">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="2667d-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-499">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-500">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="2667d-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="2667d-501">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2667d-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="2667d-502">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2667d-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="2667d-503">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2667d-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="2667d-504">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="2667d-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="2667d-505">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="2667d-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="2667d-506">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2667d-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="2667d-507">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="2667d-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="2667d-508">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="2667d-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="2667d-509">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="2667d-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2667d-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2667d-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2667d-511">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="2667d-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="2667d-512">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="2667d-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="2667d-513">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="2667d-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="2667d-514">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="2667d-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2667d-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2667d-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2667d-516">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="2667d-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2667d-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2667d-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="2667d-518">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="2667d-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2667d-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2667d-519">AzureRM.Insights</span></span>
* <span data-ttu-id="2667d-520">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2667d-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="2667d-521">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="2667d-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2667d-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2667d-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2667d-523">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-524">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-525">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="2667d-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-526">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-527">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="2667d-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="2667d-528">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="2667d-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-530">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="2667d-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="2667d-531">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="2667d-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="2667d-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-532">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-533">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2667d-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="2667d-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2667d-535">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2667d-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="2667d-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="2667d-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="2667d-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="2667d-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="2667d-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="2667d-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="2667d-539">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2667d-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="2667d-540">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="2667d-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2667d-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-541">AzureRM.Storage</span></span>
* <span data-ttu-id="2667d-542">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="2667d-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="2667d-543">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="2667d-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="2667d-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2667d-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2667d-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2667d-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2667d-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2667d-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="2667d-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2667d-547">AzureRM.Tags</span></span>
* <span data-ttu-id="2667d-548">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="2667d-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="2667d-549">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2667d-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-550">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-551">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="2667d-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2667d-552">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-552">Azure.Storage</span></span>
* <span data-ttu-id="2667d-553">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="2667d-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="2667d-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2667d-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="2667d-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2667d-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2667d-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2667d-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2667d-557">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="2667d-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2667d-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2667d-558">AzureRM.Automation</span></span>
* <span data-ttu-id="2667d-559">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="2667d-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-560">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-561">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2667d-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="2667d-562">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="2667d-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2667d-563">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="2667d-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2667d-564">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="2667d-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="2667d-565">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="2667d-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2667d-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2667d-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="2667d-567">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="2667d-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2667d-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2667d-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2667d-569">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2667d-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2667d-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2667d-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2667d-571">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2667d-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-572">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-573">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2667d-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="2667d-574">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2667d-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="2667d-575">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="2667d-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="2667d-576">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2667d-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="2667d-577">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2667d-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="2667d-578">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="2667d-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2667d-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2667d-579">AzureRM.Relay</span></span>
* <span data-ttu-id="2667d-580">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="2667d-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-581">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-582">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="2667d-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="2667d-583">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="2667d-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="2667d-584">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2667d-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="2667d-585">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="2667d-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="2667d-586">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="2667d-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-588">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="2667d-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="2667d-589">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="2667d-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="2667d-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2667d-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2667d-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2667d-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2667d-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2667d-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2667d-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2667d-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2667d-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2667d-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="2667d-595">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="2667d-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2667d-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2667d-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2667d-597">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="2667d-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2667d-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-598">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-599">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="2667d-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="2667d-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="2667d-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-602">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-603">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="2667d-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="2667d-604">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="2667d-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="2667d-605">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="2667d-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="2667d-606">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2667d-607">Generale</span><span class="sxs-lookup"><span data-stu-id="2667d-607">General</span></span>
* <span data-ttu-id="2667d-608">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="2667d-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2667d-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-609">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-610">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="2667d-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-611">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-612">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="2667d-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="2667d-613">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="2667d-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="2667d-614">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="2667d-615">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="2667d-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="2667d-616">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="2667d-617">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="2667d-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="2667d-618">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2667d-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2667d-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2667d-620">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2667d-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="2667d-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2667d-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2667d-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2667d-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2667d-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2667d-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2667d-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2667d-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2667d-625">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2667d-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="2667d-626">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="2667d-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2667d-627">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="2667d-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="2667d-628">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="2667d-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2667d-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2667d-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="2667d-630">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2667d-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="2667d-631">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="2667d-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="2667d-632">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="2667d-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="2667d-633">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2667d-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2667d-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2667d-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2667d-635">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="2667d-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-636">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-637">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="2667d-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="2667d-638">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="2667d-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="2667d-639">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2667d-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2667d-640">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2667d-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2667d-641">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2667d-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2667d-642">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2667d-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2667d-643">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2667d-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2667d-644">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2667d-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2667d-645">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2667d-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2667d-646">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2667d-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2667d-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2667d-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2667d-648">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="2667d-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="2667d-649">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2667d-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="2667d-650">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="2667d-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-651">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-652">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="2667d-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="2667d-653">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="2667d-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="2667d-654">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="2667d-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="2667d-655">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="2667d-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="2667d-656">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2667d-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="2667d-657">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="2667d-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2667d-658">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="2667d-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2667d-659">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2667d-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="2667d-660">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="2667d-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2667d-661">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="2667d-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2667d-662">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2667d-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="2667d-663">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="2667d-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="2667d-664">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="2667d-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="2667d-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2667d-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2667d-666">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2667d-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2667d-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-667">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-668">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="2667d-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="2667d-669">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="2667d-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="2667d-670">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2667d-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-671">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-672">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="2667d-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="2667d-673">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="2667d-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2667d-674">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2667d-674">Azure.Storage</span></span>
* <span data-ttu-id="2667d-675">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="2667d-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-676">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-677">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="2667d-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="2667d-678">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="2667d-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="2667d-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2667d-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2667d-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2667d-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2667d-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2667d-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2667d-682">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="2667d-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="2667d-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2667d-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="2667d-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2667d-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="2667d-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2667d-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="2667d-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2667d-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="2667d-687">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="2667d-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="2667d-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="2667d-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2667d-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="2667d-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2667d-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="2667d-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="2667d-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="2667d-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="2667d-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2667d-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="2667d-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2667d-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="2667d-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2667d-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2667d-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="2667d-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="2667d-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2667d-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2667d-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2667d-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="2667d-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2667d-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="2667d-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2667d-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2667d-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2667d-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2667d-703">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="2667d-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2667d-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2667d-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2667d-705">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="2667d-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2667d-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2667d-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2667d-707">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="2667d-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="2667d-708">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="2667d-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="2667d-709">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="2667d-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2667d-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2667d-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2667d-711">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="2667d-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="2667d-712">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="2667d-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2667d-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-713">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-714">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="2667d-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2667d-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2667d-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2667d-716">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-717">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-718">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2667d-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="2667d-719">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="2667d-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="2667d-720">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="2667d-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2667d-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2667d-722">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="2667d-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="2667d-723">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2667d-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-724">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-725">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="2667d-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2667d-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2667d-726">AzureRM.Compute</span></span>
* <span data-ttu-id="2667d-727">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="2667d-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="2667d-728">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="2667d-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="2667d-729">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="2667d-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2667d-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2667d-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2667d-731">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="2667d-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="2667d-732">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="2667d-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="2667d-733">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="2667d-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="2667d-734">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="2667d-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="2667d-735">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="2667d-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2667d-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2667d-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2667d-737">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="2667d-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2667d-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-738">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-739">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="2667d-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2667d-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2667d-740">AzureRM.Resources</span></span>
* <span data-ttu-id="2667d-741">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="2667d-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2667d-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2667d-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2667d-743">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2667d-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="2667d-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-744">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-745">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="2667d-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="2667d-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2667d-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2667d-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2667d-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2667d-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2667d-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2667d-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2667d-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2667d-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2667d-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2667d-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2667d-751">AzureRM.Websites</span></span>
* <span data-ttu-id="2667d-752">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="2667d-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="2667d-753">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="2667d-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2667d-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2667d-754">AzureRM.Profile</span></span>
* <span data-ttu-id="2667d-755">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="2667d-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2667d-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2667d-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2667d-757">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="2667d-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2667d-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2667d-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2667d-759">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="2667d-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="2667d-760">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2667d-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="2667d-761">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="2667d-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="2667d-762">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="2667d-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="2667d-763">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="2667d-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="2667d-764">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="2667d-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="2667d-765">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="2667d-765">Added support for MSI identity</span></span>
* <span data-ttu-id="2667d-766">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="2667d-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="2667d-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2667d-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="2667d-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="2667d-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2667d-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="2667d-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2667d-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2667d-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2667d-771">AzureRM.Batch</span></span>
* <span data-ttu-id="2667d-772">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="2667d-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="2667d-773">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="2667d-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2667d-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2667d-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="2667d-775">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="2667d-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2667d-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2667d-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2667d-777">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="2667d-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2667d-778">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2667d-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="2667d-779">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2667d-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="2667d-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2667d-780">AzureRM.Network</span></span>
* <span data-ttu-id="2667d-781">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="2667d-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="2667d-782">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="2667d-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="2667d-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2667d-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="2667d-784">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="2667d-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="2667d-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2667d-786">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="2667d-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="2667d-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2667d-788">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="2667d-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="2667d-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2667d-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2667d-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2667d-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2667d-791">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="2667d-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2667d-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2667d-792">AzureRM.Sql</span></span>
* <span data-ttu-id="2667d-793">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="2667d-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="2667d-794">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="2667d-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="2667d-795">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="2667d-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="2667d-796">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="2667d-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="2667d-797">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="2667d-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="2667d-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2667d-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2667d-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2667d-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2667d-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2667d-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2667d-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2667d-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2667d-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2667d-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2667d-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2667d-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2667d-804">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="2667d-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
