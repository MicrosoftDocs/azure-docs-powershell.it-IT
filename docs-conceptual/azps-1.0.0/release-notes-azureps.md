## <a name="100---december-2018"></a><span data-ttu-id="f5d7e-101">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f5d7e-102">Generale</span><span class="sxs-lookup"><span data-stu-id="f5d7e-102">General</span></span>

- <span data-ttu-id="f5d7e-103">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="f5d7e-103">General Availability of Az Module</span></span>
- <span data-ttu-id="f5d7e-104">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="f5d7e-104">Online help for each module</span></span>
- <span data-ttu-id="f5d7e-105">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f5d7e-106">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="f5d7e-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f5d7e-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5d7e-107">Az.Accounts</span></span>
- <span data-ttu-id="f5d7e-108">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="f5d7e-109">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="f5d7e-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f5d7e-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5d7e-110">Az.ApiManagement</span></span>
- <span data-ttu-id="f5d7e-111">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="f5d7e-111">Fixes for #7002</span></span>
- <span data-ttu-id="f5d7e-112">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f5d7e-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f5d7e-113">Az.Batch</span></span>
- <span data-ttu-id="f5d7e-114">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f5d7e-115">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f5d7e-116">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f5d7e-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f5d7e-117">Az.Billing</span></span>
- <span data-ttu-id="f5d7e-118">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f5d7e-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f5d7e-119">Az.CognitivServices</span></span>
- <span data-ttu-id="f5d7e-120">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f5d7e-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f5d7e-121">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f5d7e-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f5d7e-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5d7e-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="f5d7e-123">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d7e-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f5d7e-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f5d7e-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f5d7e-125">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f5d7e-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5d7e-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="f5d7e-127">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f5d7e-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f5d7e-128">Az.Monitor</span></span>
- <span data-ttu-id="f5d7e-129">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f5d7e-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5d7e-130">Az.KeyVault</span></span>
- <span data-ttu-id="f5d7e-131">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="f5d7e-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f5d7e-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f5d7e-132">Az.MachineLearning</span></span>
- <span data-ttu-id="f5d7e-133">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f5d7e-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f5d7e-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f5d7e-134">Az.Media</span></span>
- <span data-ttu-id="f5d7e-135">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f5d7e-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f5d7e-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5d7e-136">Az.Network</span></span>
<span data-ttu-id="f5d7e-137">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f5d7e-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f5d7e-138">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="f5d7e-138">New cmdlets added:</span></span>
        - <span data-ttu-id="f5d7e-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5d7e-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5d7e-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5d7e-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5d7e-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f5d7e-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f5d7e-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f5d7e-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f5d7e-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5d7e-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f5d7e-147">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f5d7e-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5d7e-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f5d7e-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f5d7e-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f5d7e-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f5d7e-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f5d7e-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f5d7e-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f5d7e-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f5d7e-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f5d7e-153">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f5d7e-154">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f5d7e-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f5d7e-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5d7e-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f5d7e-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5d7e-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f5d7e-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f5d7e-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f5d7e-158">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d7e-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f5d7e-159">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f5d7e-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f5d7e-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="f5d7e-161">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f5d7e-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-162">Az.Profile</span></span>
- <span data-ttu-id="f5d7e-163">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f5d7e-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f5d7e-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5d7e-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="f5d7e-165">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f5d7e-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5d7e-166">Az.Resources</span></span>
- <span data-ttu-id="f5d7e-167">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f5d7e-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5d7e-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="f5d7e-169">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="f5d7e-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f5d7e-170">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f5d7e-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f5d7e-171">Az.SIgnalR</span></span>
- <span data-ttu-id="f5d7e-172">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f5d7e-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f5d7e-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5d7e-173">Az.Sql</span></span>
- <span data-ttu-id="f5d7e-174">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="f5d7e-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f5d7e-175">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="f5d7e-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f5d7e-176">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f5d7e-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5d7e-177">Az.Storage</span></span>
- <span data-ttu-id="f5d7e-178">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f5d7e-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5d7e-179">Az.Websites</span></span>
- <span data-ttu-id="f5d7e-180">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f5d7e-181">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f5d7e-182">Generale</span><span class="sxs-lookup"><span data-stu-id="f5d7e-182">General</span></span>

* <span data-ttu-id="f5d7e-183">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="f5d7e-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f5d7e-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5d7e-184">Az.Compute</span></span>

* <span data-ttu-id="f5d7e-185">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f5d7e-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5d7e-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="f5d7e-187">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="f5d7e-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f5d7e-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f5d7e-188">Az.FrontDoor</span></span>

* <span data-ttu-id="f5d7e-189">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="f5d7e-189">Fixed some broken links</span></span>
    - <span data-ttu-id="f5d7e-190">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f5d7e-191">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f5d7e-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f5d7e-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="f5d7e-193">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f5d7e-194">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f5d7e-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5d7e-195">Az.Resources</span></span>

* <span data-ttu-id="f5d7e-196">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f5d7e-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f5d7e-197">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f5d7e-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5d7e-198">Az.Sql</span></span>

* <span data-ttu-id="f5d7e-199">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="f5d7e-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f5d7e-200">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="f5d7e-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f5d7e-201">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f5d7e-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f5d7e-202">Az.Storage</span></span>

* <span data-ttu-id="f5d7e-203">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5d7e-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f5d7e-204">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="f5d7e-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f5d7e-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5d7e-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f5d7e-206">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="f5d7e-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="f5d7e-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5d7e-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f5d7e-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f5d7e-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f5d7e-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5d7e-209">Az.Websites</span></span>

* <span data-ttu-id="f5d7e-210">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f5d7e-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f5d7e-211">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f5d7e-212">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f5d7e-213">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f5d7e-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f5d7e-214">Az.ApiManagement</span></span>
* <span data-ttu-id="f5d7e-215">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f5d7e-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f5d7e-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f5d7e-216">Az.Automation</span></span>
* <span data-ttu-id="f5d7e-217">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="f5d7e-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f5d7e-218">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="f5d7e-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f5d7e-219">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="f5d7e-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f5d7e-220">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="f5d7e-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f5d7e-221">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="f5d7e-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f5d7e-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5d7e-222">Az.Compute</span></span>
* <span data-ttu-id="f5d7e-223">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f5d7e-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f5d7e-224">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f5d7e-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f5d7e-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f5d7e-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="f5d7e-226">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f5d7e-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f5d7e-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f5d7e-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f5d7e-228">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="f5d7e-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f5d7e-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5d7e-229">Az.Network</span></span>
* <span data-ttu-id="f5d7e-230">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f5d7e-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f5d7e-231">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="f5d7e-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f5d7e-232">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f5d7e-233">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f5d7e-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f5d7e-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f5d7e-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f5d7e-235">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f5d7e-236">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f5d7e-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f5d7e-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f5d7e-238">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f5d7e-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f5d7e-239">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="f5d7e-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f5d7e-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f5d7e-240">Az.Relay</span></span>
* <span data-ttu-id="f5d7e-241">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f5d7e-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5d7e-242">Az.Resources</span></span>
* <span data-ttu-id="f5d7e-243">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f5d7e-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f5d7e-244">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="f5d7e-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f5d7e-245">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f5d7e-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f5d7e-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5d7e-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5d7e-247">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="f5d7e-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f5d7e-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5d7e-248">Az.Sql</span></span>
* <span data-ttu-id="f5d7e-249">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="f5d7e-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f5d7e-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5d7e-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5d7e-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5d7e-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5d7e-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5d7e-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5d7e-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f5d7e-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f5d7e-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5d7e-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5d7e-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5d7e-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5d7e-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5d7e-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f5d7e-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f5d7e-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f5d7e-258">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f5d7e-259">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f5d7e-260">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f5d7e-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f5d7e-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f5d7e-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f5d7e-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f5d7e-265">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f5d7e-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f5d7e-266">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f5d7e-267">Generale</span><span class="sxs-lookup"><span data-stu-id="f5d7e-267">General</span></span>
* <span data-ttu-id="f5d7e-268">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="f5d7e-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f5d7e-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-269">Az.Profile</span></span>
* <span data-ttu-id="f5d7e-270">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f5d7e-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f5d7e-271">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="f5d7e-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f5d7e-272">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f5d7e-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f5d7e-273">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="f5d7e-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f5d7e-274">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="f5d7e-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f5d7e-275">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="f5d7e-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f5d7e-276">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="f5d7e-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f5d7e-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5d7e-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5d7e-278">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5d7e-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5d7e-279">Az.Compute</span></span>
* <span data-ttu-id="f5d7e-280">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f5d7e-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f5d7e-281">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f5d7e-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f5d7e-282">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5d7e-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5d7e-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5d7e-284">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f5d7e-285">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f5d7e-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f5d7e-286">Az.Insights</span></span>
* <span data-ttu-id="f5d7e-287">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="f5d7e-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f5d7e-288">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="f5d7e-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f5d7e-289">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="f5d7e-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f5d7e-290">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="f5d7e-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5d7e-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5d7e-291">Az.Network</span></span>
* <span data-ttu-id="f5d7e-292">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5d7e-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f5d7e-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5d7e-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f5d7e-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f5d7e-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f5d7e-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5d7e-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f5d7e-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f5d7e-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f5d7e-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5d7e-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f5d7e-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5d7e-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f5d7e-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f5d7e-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="f5d7e-300">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="f5d7e-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5d7e-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5d7e-301">Az.Resources</span></span>
* <span data-ttu-id="f5d7e-302">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f5d7e-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f5d7e-303">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f5d7e-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f5d7e-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f5d7e-304">Az.ServiceBus</span></span>
* <span data-ttu-id="f5d7e-305">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f5d7e-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f5d7e-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="f5d7e-307">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f5d7e-308">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="f5d7e-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f5d7e-309">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f5d7e-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f5d7e-310">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f5d7e-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f5d7e-311">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f5d7e-312">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f5d7e-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-313">Az.Profile</span></span>
* <span data-ttu-id="f5d7e-314">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="f5d7e-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f5d7e-315">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f5d7e-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5d7e-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5d7e-316">Az.Compute</span></span>
* <span data-ttu-id="f5d7e-317">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="f5d7e-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f5d7e-318">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f5d7e-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f5d7e-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="f5d7e-320">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f5d7e-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f5d7e-321">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f5d7e-322">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f5d7e-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f5d7e-324">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5d7e-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5d7e-325">Az.Network</span></span>
* <span data-ttu-id="f5d7e-326">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f5d7e-327">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5d7e-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5d7e-328">Az.Resources</span></span>
* <span data-ttu-id="f5d7e-329">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f5d7e-330">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f5d7e-331">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f5d7e-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f5d7e-332">Azure.Storage</span></span>
* <span data-ttu-id="f5d7e-333">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="f5d7e-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f5d7e-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f5d7e-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f5d7e-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f5d7e-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f5d7e-336">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="f5d7e-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f5d7e-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f5d7e-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f5d7e-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f5d7e-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="f5d7e-339">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f5d7e-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f5d7e-340">Az.Compute</span></span>
* <span data-ttu-id="f5d7e-341">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="f5d7e-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f5d7e-342">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f5d7e-343">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="f5d7e-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f5d7e-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f5d7e-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f5d7e-345">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="f5d7e-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f5d7e-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f5d7e-346">Az.Network</span></span>
* <span data-ttu-id="f5d7e-347">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f5d7e-348">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-348">new cmdlets added</span></span>
    - <span data-ttu-id="f5d7e-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5d7e-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5d7e-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5d7e-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f5d7e-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f5d7e-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f5d7e-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f5d7e-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5d7e-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f5d7e-355">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="f5d7e-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f5d7e-356">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f5d7e-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f5d7e-357">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f5d7e-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f5d7e-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f5d7e-358">Az.RedisCache</span></span>
* <span data-ttu-id="f5d7e-359">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="f5d7e-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f5d7e-360">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f5d7e-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f5d7e-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f5d7e-361">Az.Resources</span></span>
* <span data-ttu-id="f5d7e-362">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f5d7e-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f5d7e-363">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="f5d7e-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f5d7e-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f5d7e-364">Az.Sql</span></span>
* <span data-ttu-id="f5d7e-365">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="f5d7e-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f5d7e-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f5d7e-366">Az.Websites</span></span>
* <span data-ttu-id="f5d7e-367">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="f5d7e-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f5d7e-368">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="f5d7e-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f5d7e-369">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="f5d7e-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f5d7e-370">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="f5d7e-370">Initial Release</span></span>