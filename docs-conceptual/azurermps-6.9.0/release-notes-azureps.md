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
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179004"
---
# <a name="release-notes"></a><span data-ttu-id="400a5-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="400a5-103">Release notes</span></span>

<span data-ttu-id="400a5-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="400a5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="400a5-105">6.9.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="400a5-106">Generale</span><span class="sxs-lookup"><span data-stu-id="400a5-106">General</span></span>
* <span data-ttu-id="400a5-107">Aggiunta di AzureRM.SignalR al modulo di rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="400a5-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="400a5-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-108">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-109">Modifiche minori al codice comune di archiviazione</span><span class="sxs-lookup"><span data-stu-id="400a5-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="400a5-110">Aggiornamento dei file della Guida per includere tipi di parametri completi.</span><span class="sxs-lookup"><span data-stu-id="400a5-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="400a5-111">Modifica di -ServicePrincipal in non obbligatorio nel set di parametri ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="400a5-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="400a5-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-112">Azure.Storage</span></span>
* <span data-ttu-id="400a5-113">Supporto della creazione del contesto di archiviazione con OAuth.</span><span class="sxs-lookup"><span data-stu-id="400a5-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="400a5-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="400a5-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="400a5-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="400a5-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="400a5-116">Aggiunta di Standard_Microsoft nello SKU del piano tariffario per la rete CDN.</span><span class="sxs-lookup"><span data-stu-id="400a5-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-117">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-118">Trasferimento delle dipendenze da Key Vault e Archiviazione a dipendenze comuni</span><span class="sxs-lookup"><span data-stu-id="400a5-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="400a5-119">Aggiunta del supporto per altre dimensioni delle macchine virtuali ai cmdlet AEM</span><span class="sxs-lookup"><span data-stu-id="400a5-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="400a5-120">Aggiunta del parametro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="400a5-121">Aggiunta del parametro ResourceId a Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="400a5-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="400a5-122">Aggiunta del cmdlet Invoke-AzureRmVmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="400a5-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="400a5-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="400a5-123">AzureRM.Dns</span></span>
* <span data-ttu-id="400a5-124">Aggiunta del supporto per record alias durante la creazione del record DNS</span><span class="sxs-lookup"><span data-stu-id="400a5-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="400a5-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="400a5-125">AzureRM.Insights</span></span>
* <span data-ttu-id="400a5-126">Risoluzione dei problemi 6833 e 7102 (area Impostazioni di diagnostica)</span><span class="sxs-lookup"><span data-stu-id="400a5-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="400a5-127">Problemi con il nome predefinito, ovvero 'service', durante la creazione e l'elencazione/ottenimento delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="400a5-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="400a5-128">Problemi nella creazione di impostazioni di diagnostica con categorie</span><span class="sxs-lookup"><span data-stu-id="400a5-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="400a5-129">Aggiunta del messaggio di funzione deprecata per i parametri degli intervalli di tempo delle metriche</span><span class="sxs-lookup"><span data-stu-id="400a5-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="400a5-130">I parametri timegrains vengono ancora accettati (si tratta di una modifica che non causa interruzioni), ma vengono ignorati nel back-end perché solo PT1M è valido</span><span class="sxs-lookup"><span data-stu-id="400a5-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-131">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-132">Modifiche ai cmdlet LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="400a5-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="400a5-133">LoadBalancerInboundNatPoolConfig: aggiunta dei parametri IdleTimeoutInMinutes, EnableFloatingIp ed EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="400a5-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="400a5-134">LoadBalancerInboundNatRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="400a5-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="400a5-135">LoadBalancerRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="400a5-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="400a5-136">LoadBalancerProbeConfig: aggiunta del supporto del valore "Https" per il parametro Protocol</span><span class="sxs-lookup"><span data-stu-id="400a5-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="400a5-137">Aggiunta di nuovi comandi per la nuova OutboundRule delle sottorisorse di LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="400a5-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="400a5-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="400a5-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="400a5-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="400a5-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="400a5-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="400a5-143">Aggiunta della nuova proprietà HostedWorkloads per PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="400a5-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="400a5-144">Aggiunta di nuovi cmdlet per la funzionalità Firewall di Azure tramite ARM</span><span class="sxs-lookup"><span data-stu-id="400a5-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="400a5-145">Aggiunta di Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="400a5-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="400a5-146">Aggiunta di Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="400a5-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="400a5-147">Aggiunta di New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="400a5-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="400a5-148">Aggiunta di Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="400a5-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="400a5-149">Aggiunta di New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="400a5-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="400a5-150">Aggiunta di New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="400a5-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="400a5-151">Aggiunta di New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="400a5-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="400a5-152">Aggiunta di New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="400a5-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="400a5-153">Aggiunta di New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="400a5-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="400a5-154">Aggiunta di New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="400a5-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="400a5-155">Aggiunta del supporto per il certificato radice attendibile e la configurazione della scalabilità automatica nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="400a5-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="400a5-156">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="400a5-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="400a5-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="400a5-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="400a5-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="400a5-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="400a5-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="400a5-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="400a5-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="400a5-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="400a5-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="400a5-166">Aggiornamento dei cmdlet con il parametro facoltativo -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="400a5-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="400a5-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="400a5-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="400a5-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="400a5-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="400a5-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="400a5-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="400a5-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="400a5-171">Aggiornamento dei cmdlet con il parametro facoltativo -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="400a5-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="400a5-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="400a5-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="400a5-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="400a5-174">Aggiunta di un cmdlet per l'endpoint di interfaccia Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="400a5-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="400a5-175">Aggiunta del supporto per più prefissi di indirizzi in una sottorete.</span><span class="sxs-lookup"><span data-stu-id="400a5-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="400a5-176">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="400a5-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="400a5-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="400a5-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="400a5-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="400a5-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="400a5-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="400a5-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="400a5-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="400a5-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="400a5-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="400a5-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="400a5-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="400a5-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="400a5-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="400a5-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="400a5-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="400a5-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="400a5-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="400a5-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="400a5-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="400a5-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="400a5-196">Aggiunta di cmdlet per la delega di subnet.</span><span class="sxs-lookup"><span data-stu-id="400a5-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="400a5-197">New-AzureRmDelegation: crea una nuova delega che può essere aggiunta a una subnet</span><span class="sxs-lookup"><span data-stu-id="400a5-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="400a5-198">Remove-AzureRmDelegation: acquisisce una subnet e rimuove il nome di delega fornito da tale subnet</span><span class="sxs-lookup"><span data-stu-id="400a5-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="400a5-199">Add-AzureRmDelegation: acquisisce una subnet e aggiunge il nome servizio specificato come delega a tale subnet</span><span class="sxs-lookup"><span data-stu-id="400a5-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="400a5-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="400a5-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="400a5-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="400a5-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="400a5-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="400a5-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="400a5-203">Supporto per dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="400a5-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="400a5-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="400a5-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="400a5-205">Aggiornamento della dipendenza di Insights.</span><span class="sxs-lookup"><span data-stu-id="400a5-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-206">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-207">Aggiornamento di New-AzureRmResourceGroupDeployment con il nuovo parametro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="400a5-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="400a5-208">Aggiunta del supporto per OnErrorDeployment con il nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="400a5-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="400a5-209">Supporto dell'identità gestita per le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="400a5-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="400a5-210">Non sono più necessari parametri con valori predefiniti durante l'assegnazione di criteri con 'New-AzureRmPolicyAssignment'</span><span class="sxs-lookup"><span data-stu-id="400a5-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="400a5-211">Aggiunta del nuovo cmdlet Get-AzureRmPolicyAlias per il recupero di alias dei criteri</span><span class="sxs-lookup"><span data-stu-id="400a5-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-213">Risoluzione del problema #7161</span><span class="sxs-lookup"><span data-stu-id="400a5-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="400a5-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="400a5-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="400a5-215">Aggiornamento dei nomi SKU in Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="400a5-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="400a5-216">Aggiunta del campo di versione all'oggetto PSSignalRResource e della stringa di connessione all'oggetto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="400a5-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="400a5-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-217">AzureRM.Storage</span></span>
* <span data-ttu-id="400a5-218">Supporto dei criteri di immutabilità in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="400a5-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="400a5-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="400a5-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="400a5-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="400a5-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="400a5-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="400a5-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="400a5-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="400a5-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="400a5-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="400a5-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="400a5-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="400a5-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="400a5-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="400a5-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="400a5-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="400a5-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="400a5-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="400a5-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="400a5-230">AzureRM.Websites</span></span>
* <span data-ttu-id="400a5-231">Aggiunta di due nuovi cmdlet: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="400a5-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="400a5-232">New-AzureRmAppServicePlan - Aggiunta dello switch HyperV per la creazione di un piano del servizio app con il contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="400a5-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="400a5-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Aggiunta di nuovi parametri (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) per la creazione e la gestione di app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="400a5-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="400a5-234">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="400a5-235">Generale</span><span class="sxs-lookup"><span data-stu-id="400a5-235">General</span></span>
* <span data-ttu-id="400a5-236">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="400a5-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="400a5-237">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="400a5-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="400a5-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="400a5-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="400a5-239">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="400a5-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="400a5-240">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="400a5-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="400a5-241">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="400a5-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="400a5-242">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="400a5-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="400a5-243">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="400a5-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="400a5-244">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="400a5-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="400a5-245">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="400a5-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="400a5-246">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="400a5-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="400a5-247">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="400a5-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="400a5-248">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="400a5-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="400a5-249">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="400a5-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="400a5-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-250">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-251">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="400a5-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="400a5-252">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="400a5-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="400a5-253">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="400a5-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="400a5-254">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="400a5-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-255">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-256">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="400a5-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="400a5-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="400a5-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="400a5-258">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="400a5-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="400a5-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-259">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-260">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="400a5-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-262">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="400a5-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="400a5-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="400a5-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="400a5-264">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="400a5-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="400a5-265">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="400a5-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="400a5-266">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="400a5-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="400a5-267">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="400a5-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="400a5-268">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="400a5-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="400a5-269">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="400a5-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="400a5-270">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="400a5-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="400a5-271">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="400a5-272">Generale</span><span class="sxs-lookup"><span data-stu-id="400a5-272">General</span></span>
* <span data-ttu-id="400a5-273">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="400a5-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="400a5-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-274">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-275">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="400a5-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-276">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-277">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="400a5-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="400a5-278">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="400a5-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="400a5-279">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="400a5-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="400a5-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="400a5-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="400a5-281">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="400a5-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-282">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-283">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="400a5-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="400a5-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="400a5-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="400a5-285">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="400a5-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-286">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-287">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="400a5-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-289">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="400a5-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="400a5-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="400a5-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="400a5-291">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="400a5-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="400a5-292">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="400a5-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="400a5-293">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="400a5-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="400a5-294">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="400a5-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="400a5-295">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="400a5-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="400a5-296">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="400a5-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="400a5-297">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="400a5-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="400a5-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="400a5-298">AzureRM.Websites</span></span>
* <span data-ttu-id="400a5-299">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="400a5-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="400a5-300">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="400a5-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-301">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-302">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="400a5-303">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="400a5-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="400a5-304">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="400a5-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="400a5-305">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="400a5-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="400a5-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-306">Azure.Storage</span></span>
* <span data-ttu-id="400a5-307">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="400a5-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="400a5-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="400a5-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="400a5-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="400a5-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="400a5-310">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="400a5-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="400a5-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="400a5-312">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="400a5-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="400a5-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="400a5-314">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="400a5-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="400a5-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="400a5-316">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="400a5-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="400a5-317">AzureRM.Automation</span></span>
* <span data-ttu-id="400a5-318">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="400a5-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="400a5-319">AzureRM.Backup</span></span>
* <span data-ttu-id="400a5-320">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="400a5-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="400a5-321">AzureRM.Batch</span></span>
* <span data-ttu-id="400a5-322">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="400a5-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="400a5-323">AzureRM.Billing</span></span>
* <span data-ttu-id="400a5-324">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="400a5-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="400a5-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="400a5-326">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="400a5-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="400a5-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="400a5-328">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-329">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-330">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="400a5-331">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="400a5-332">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="400a5-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="400a5-333">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="400a5-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="400a5-334">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="400a5-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="400a5-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="400a5-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="400a5-336">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="400a5-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="400a5-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="400a5-338">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="400a5-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="400a5-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="400a5-340">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="400a5-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="400a5-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="400a5-342">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="400a5-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="400a5-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="400a5-344">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="400a5-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="400a5-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="400a5-346">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="400a5-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="400a5-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="400a5-348">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="400a5-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="400a5-349">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="400a5-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="400a5-350">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="400a5-351">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="400a5-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="400a5-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="400a5-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="400a5-353">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="400a5-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="400a5-354">AzureRM.Dns</span></span>
* <span data-ttu-id="400a5-355">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="400a5-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="400a5-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="400a5-357">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="400a5-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="400a5-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="400a5-359">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="400a5-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="400a5-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="400a5-361">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="400a5-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="400a5-362">AzureRM.Insights</span></span>
* <span data-ttu-id="400a5-363">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="400a5-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="400a5-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="400a5-365">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="400a5-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="400a5-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="400a5-367">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="400a5-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="400a5-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="400a5-369">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="400a5-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="400a5-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="400a5-371">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="400a5-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="400a5-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="400a5-373">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="400a5-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="400a5-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="400a5-375">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="400a5-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="400a5-376">AzureRM.Media</span></span>
* <span data-ttu-id="400a5-377">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-378">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-379">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="400a5-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="400a5-380">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="400a5-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="400a5-381">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="400a5-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="400a5-382">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="400a5-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="400a5-383">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="400a5-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="400a5-384">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="400a5-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="400a5-385">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="400a5-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="400a5-386">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="400a5-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="400a5-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="400a5-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="400a5-388">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="400a5-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="400a5-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="400a5-390">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="400a5-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="400a5-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="400a5-392">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="400a5-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="400a5-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="400a5-394">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="400a5-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="400a5-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="400a5-396">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="400a5-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="400a5-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="400a5-398">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="400a5-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="400a5-399">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="400a5-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="400a5-400">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="400a5-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="400a5-401">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="400a5-402">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="400a5-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="400a5-403">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="400a5-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="400a5-404">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="400a5-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="400a5-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="400a5-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="400a5-406">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="400a5-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="400a5-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="400a5-408">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="400a5-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="400a5-409">AzureRM.Relay</span></span>
* <span data-ttu-id="400a5-410">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-411">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-412">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="400a5-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="400a5-413">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="400a5-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="400a5-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="400a5-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="400a5-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="400a5-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="400a5-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="400a5-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="400a5-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="400a5-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="400a5-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="400a5-421">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="400a5-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="400a5-422">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="400a5-423">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="400a5-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="400a5-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="400a5-425">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-427">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="400a5-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="400a5-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="400a5-429">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="400a5-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-430">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-431">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="400a5-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-432">AzureRM.Storage</span></span>
* <span data-ttu-id="400a5-433">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="400a5-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="400a5-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="400a5-435">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="400a5-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="400a5-436">AzureRM.Tags</span></span>
* <span data-ttu-id="400a5-437">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="400a5-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="400a5-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="400a5-439">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="400a5-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="400a5-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="400a5-441">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="400a5-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="400a5-442">AzureRM.Websites</span></span>
* <span data-ttu-id="400a5-443">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="400a5-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="400a5-444">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="400a5-445">Generale</span><span class="sxs-lookup"><span data-stu-id="400a5-445">General</span></span>
* <span data-ttu-id="400a5-446">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="400a5-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="400a5-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-447">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-448">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="400a5-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="400a5-449">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="400a5-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-450">Azure.Storage</span></span>
* <span data-ttu-id="400a5-451">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400a5-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="400a5-452">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="400a5-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="400a5-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="400a5-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="400a5-454">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="400a5-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="400a5-455">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="400a5-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="400a5-456">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="400a5-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="400a5-457">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="400a5-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="400a5-458">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="400a5-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="400a5-459">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="400a5-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-460">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-461">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="400a5-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="400a5-462">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="400a5-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="400a5-463">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="400a5-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="400a5-464">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="400a5-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="400a5-465">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="400a5-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="400a5-466">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="400a5-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="400a5-467">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="400a5-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="400a5-468">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="400a5-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="400a5-469">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="400a5-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="400a5-470">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="400a5-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="400a5-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="400a5-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="400a5-472">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="400a5-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="400a5-473">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="400a5-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="400a5-474">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="400a5-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="400a5-475">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="400a5-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="400a5-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="400a5-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="400a5-477">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="400a5-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="400a5-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="400a5-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="400a5-479">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="400a5-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="400a5-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="400a5-480">AzureRM.Insights</span></span>
* <span data-ttu-id="400a5-481">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="400a5-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="400a5-482">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="400a5-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="400a5-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="400a5-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="400a5-484">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-485">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-486">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="400a5-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-487">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-488">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="400a5-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="400a5-489">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="400a5-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-491">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="400a5-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="400a5-492">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="400a5-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="400a5-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-493">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-494">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="400a5-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="400a5-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="400a5-496">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="400a5-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="400a5-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="400a5-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="400a5-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="400a5-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="400a5-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="400a5-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="400a5-500">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="400a5-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="400a5-501">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="400a5-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="400a5-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-502">AzureRM.Storage</span></span>
* <span data-ttu-id="400a5-503">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="400a5-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="400a5-504">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="400a5-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="400a5-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="400a5-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="400a5-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="400a5-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="400a5-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="400a5-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="400a5-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="400a5-508">AzureRM.Tags</span></span>
* <span data-ttu-id="400a5-509">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="400a5-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="400a5-510">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="400a5-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-511">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-512">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="400a5-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="400a5-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-513">Azure.Storage</span></span>
* <span data-ttu-id="400a5-514">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="400a5-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="400a5-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="400a5-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="400a5-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="400a5-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="400a5-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="400a5-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="400a5-518">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="400a5-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="400a5-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="400a5-519">AzureRM.Automation</span></span>
* <span data-ttu-id="400a5-520">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="400a5-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-521">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-522">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="400a5-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="400a5-523">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="400a5-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="400a5-524">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="400a5-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="400a5-525">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="400a5-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="400a5-526">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="400a5-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="400a5-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="400a5-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="400a5-528">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="400a5-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="400a5-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="400a5-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="400a5-530">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="400a5-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="400a5-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="400a5-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="400a5-532">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="400a5-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-533">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-534">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="400a5-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="400a5-535">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="400a5-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="400a5-536">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="400a5-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="400a5-537">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="400a5-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="400a5-538">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="400a5-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="400a5-539">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="400a5-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="400a5-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="400a5-540">AzureRM.Relay</span></span>
* <span data-ttu-id="400a5-541">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="400a5-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-542">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-543">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="400a5-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="400a5-544">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="400a5-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="400a5-545">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="400a5-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="400a5-546">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="400a5-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="400a5-547">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="400a5-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-549">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="400a5-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="400a5-550">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="400a5-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="400a5-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="400a5-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="400a5-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="400a5-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="400a5-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="400a5-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="400a5-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="400a5-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="400a5-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="400a5-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="400a5-556">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="400a5-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="400a5-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="400a5-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="400a5-558">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="400a5-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="400a5-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-559">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-560">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="400a5-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="400a5-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="400a5-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="400a5-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="400a5-563">AzureRM.Websites</span></span>
* <span data-ttu-id="400a5-564">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="400a5-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="400a5-565">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="400a5-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="400a5-566">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="400a5-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="400a5-567">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="400a5-568">Generale</span><span class="sxs-lookup"><span data-stu-id="400a5-568">General</span></span>
* <span data-ttu-id="400a5-569">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="400a5-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="400a5-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-570">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-571">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="400a5-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-572">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-573">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="400a5-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="400a5-574">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="400a5-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="400a5-575">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="400a5-576">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="400a5-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="400a5-577">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="400a5-578">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="400a5-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="400a5-579">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="400a5-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="400a5-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="400a5-581">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="400a5-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="400a5-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="400a5-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="400a5-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="400a5-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="400a5-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="400a5-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="400a5-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="400a5-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="400a5-586">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="400a5-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="400a5-587">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="400a5-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="400a5-588">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="400a5-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="400a5-589">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="400a5-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="400a5-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="400a5-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="400a5-591">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="400a5-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="400a5-592">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="400a5-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="400a5-593">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="400a5-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="400a5-594">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="400a5-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="400a5-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="400a5-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="400a5-596">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="400a5-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-597">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-598">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="400a5-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="400a5-599">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="400a5-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="400a5-600">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="400a5-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="400a5-601">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="400a5-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="400a5-602">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="400a5-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="400a5-603">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="400a5-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="400a5-604">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="400a5-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="400a5-605">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="400a5-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="400a5-606">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="400a5-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="400a5-607">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="400a5-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="400a5-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="400a5-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="400a5-609">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="400a5-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="400a5-610">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="400a5-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="400a5-611">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="400a5-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-612">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-613">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="400a5-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="400a5-614">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="400a5-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="400a5-615">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="400a5-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="400a5-616">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="400a5-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="400a5-617">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="400a5-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="400a5-618">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="400a5-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="400a5-619">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="400a5-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="400a5-620">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="400a5-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="400a5-621">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="400a5-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="400a5-622">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="400a5-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="400a5-623">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="400a5-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="400a5-624">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="400a5-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="400a5-625">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="400a5-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="400a5-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="400a5-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="400a5-627">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="400a5-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="400a5-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-628">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-629">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="400a5-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="400a5-630">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="400a5-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="400a5-631">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="400a5-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-632">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-633">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="400a5-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="400a5-634">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="400a5-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="400a5-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="400a5-635">Azure.Storage</span></span>
* <span data-ttu-id="400a5-636">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="400a5-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-637">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-638">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="400a5-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="400a5-639">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="400a5-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="400a5-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="400a5-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="400a5-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="400a5-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="400a5-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="400a5-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="400a5-643">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="400a5-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="400a5-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="400a5-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="400a5-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="400a5-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="400a5-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="400a5-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="400a5-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="400a5-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="400a5-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="400a5-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="400a5-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="400a5-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="400a5-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="400a5-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="400a5-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="400a5-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="400a5-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="400a5-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="400a5-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="400a5-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="400a5-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="400a5-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="400a5-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="400a5-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="400a5-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="400a5-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="400a5-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="400a5-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="400a5-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="400a5-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="400a5-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="400a5-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="400a5-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="400a5-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="400a5-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="400a5-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="400a5-664">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="400a5-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="400a5-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="400a5-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="400a5-666">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="400a5-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="400a5-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="400a5-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="400a5-668">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="400a5-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="400a5-669">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="400a5-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="400a5-670">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="400a5-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="400a5-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="400a5-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="400a5-672">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="400a5-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="400a5-673">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="400a5-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="400a5-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-674">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-675">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="400a5-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="400a5-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="400a5-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="400a5-677">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="400a5-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="400a5-678">AzureRM.Websites</span></span>
* <span data-ttu-id="400a5-679">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="400a5-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="400a5-680">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="400a5-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="400a5-681">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="400a5-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="400a5-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="400a5-683">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="400a5-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="400a5-684">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="400a5-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-685">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-686">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="400a5-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="400a5-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="400a5-687">AzureRM.Compute</span></span>
* <span data-ttu-id="400a5-688">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="400a5-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="400a5-689">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="400a5-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="400a5-690">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="400a5-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="400a5-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="400a5-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="400a5-692">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="400a5-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="400a5-693">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="400a5-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="400a5-694">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="400a5-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="400a5-695">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="400a5-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="400a5-696">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="400a5-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="400a5-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="400a5-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="400a5-698">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="400a5-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="400a5-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-699">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-700">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="400a5-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="400a5-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="400a5-701">AzureRM.Resources</span></span>
* <span data-ttu-id="400a5-702">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="400a5-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="400a5-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="400a5-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="400a5-704">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="400a5-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="400a5-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-705">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-706">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="400a5-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="400a5-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="400a5-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="400a5-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="400a5-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="400a5-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="400a5-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="400a5-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="400a5-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="400a5-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="400a5-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="400a5-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="400a5-712">AzureRM.Websites</span></span>
* <span data-ttu-id="400a5-713">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="400a5-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="400a5-714">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="400a5-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="400a5-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="400a5-715">AzureRM.Profile</span></span>
* <span data-ttu-id="400a5-716">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="400a5-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="400a5-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="400a5-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="400a5-718">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="400a5-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="400a5-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="400a5-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="400a5-720">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="400a5-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="400a5-721">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="400a5-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="400a5-722">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="400a5-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="400a5-723">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="400a5-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="400a5-724">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="400a5-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="400a5-725">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="400a5-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="400a5-726">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="400a5-726">Added support for MSI identity</span></span>
* <span data-ttu-id="400a5-727">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="400a5-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="400a5-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="400a5-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="400a5-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="400a5-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="400a5-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="400a5-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="400a5-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="400a5-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="400a5-732">AzureRM.Batch</span></span>
* <span data-ttu-id="400a5-733">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="400a5-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="400a5-734">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="400a5-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="400a5-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="400a5-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="400a5-736">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="400a5-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="400a5-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="400a5-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="400a5-738">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="400a5-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="400a5-739">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="400a5-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="400a5-740">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="400a5-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="400a5-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="400a5-741">AzureRM.Network</span></span>
* <span data-ttu-id="400a5-742">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="400a5-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="400a5-743">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="400a5-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="400a5-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="400a5-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="400a5-745">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="400a5-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="400a5-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="400a5-747">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="400a5-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="400a5-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="400a5-749">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="400a5-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="400a5-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="400a5-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="400a5-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="400a5-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="400a5-752">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="400a5-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="400a5-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="400a5-753">AzureRM.Sql</span></span>
* <span data-ttu-id="400a5-754">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="400a5-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="400a5-755">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="400a5-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="400a5-756">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="400a5-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="400a5-757">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="400a5-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="400a5-758">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="400a5-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="400a5-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="400a5-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="400a5-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="400a5-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="400a5-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="400a5-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="400a5-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="400a5-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="400a5-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="400a5-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="400a5-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="400a5-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="400a5-765">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="400a5-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
