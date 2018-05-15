# <a name="table-of-contents"></a><span data-ttu-id="3fe6b-101">Sommario</span><span class="sxs-lookup"><span data-stu-id="3fe6b-101">Table of Contents</span></span>
1. [<span data-ttu-id="3fe6b-102">Rimozione dei parametri Force</span><span class="sxs-lookup"><span data-stu-id="3fe6b-102">Removal of Force parameters</span></span>](#removal-of-force-parameters)
2. [<span data-ttu-id="3fe6b-103">Modifica dei parametri Tag</span><span class="sxs-lookup"><span data-stu-id="3fe6b-103">Change of Tag parameters</span></span>](#change-of-tag-parameters)
3. [<span data-ttu-id="3fe6b-104">Modifiche di rilievo ai cmdlet per Archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fe6b-104">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
4. [<span data-ttu-id="3fe6b-105">Modifiche di rilievo ai cmdlet per AD</span><span class="sxs-lookup"><span data-stu-id="3fe6b-105">Breaking changes to AD cmdlets</span></span>](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a><span data-ttu-id="3fe6b-106">Rimozione dei parametri Force</span><span class="sxs-lookup"><span data-stu-id="3fe6b-106">Removal of Force parameters</span></span>

<span data-ttu-id="3fe6b-107">In questa versione sono stati rimossi tutti i parametri `Force` obsoleti dai cmdlet, nonché i corrispondenti avvisi relativi alla rimozione del parametro in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-107">This release, we removed all Obsolete `Force` parameters from cmdlets and the corresponding warnings that the parameter would be removed in a future release.</span></span>

<span data-ttu-id="3fe6b-108">I cmdlet interessati da questa modifica sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fe6b-108">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="3fe6b-109">**Gestione API**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-109">**ApiManagement**</span></span>
- <span data-ttu-id="3fe6b-110">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3fe6b-110">Remove-AzureRmApiManagement</span></span>
- <span data-ttu-id="3fe6b-111">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3fe6b-111">Remove-AzureRmApiManagementApi</span></span>
- <span data-ttu-id="3fe6b-112">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3fe6b-112">Remove-AzureRmApiManagementGroup</span></span>
- <span data-ttu-id="3fe6b-113">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3fe6b-113">Remove-AzureRmApiManagementLogger</span></span>
- <span data-ttu-id="3fe6b-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3fe6b-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>
- <span data-ttu-id="3fe6b-115">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="3fe6b-115">Remove-AzureRmApiManagementOperation</span></span>
- <span data-ttu-id="3fe6b-116">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3fe6b-116">Remove-AzureRmApiManagementPolicy</span></span>
- <span data-ttu-id="3fe6b-117">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3fe6b-117">Remove-AzureRmApiManagementProduct</span></span>
- <span data-ttu-id="3fe6b-118">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3fe6b-118">Remove-AzureRmApiManagementProperty</span></span>
- <span data-ttu-id="3fe6b-119">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3fe6b-119">Remove-AzureRmApiManagementSubscription</span></span>
- <span data-ttu-id="3fe6b-120">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3fe6b-120">Remove-AzureRmApiManagementUser</span></span>

<span data-ttu-id="3fe6b-121">**Automazione**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-121">**Automation**</span></span>
- <span data-ttu-id="3fe6b-122">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe6b-122">Remove-AzureRmAutomationCertificate</span></span>
- <span data-ttu-id="3fe6b-123">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3fe6b-123">Remove-AzureRmAutomationCredential</span></span>
- <span data-ttu-id="3fe6b-124">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="3fe6b-124">Remove-AzureRmAutomationVariable</span></span>
- <span data-ttu-id="3fe6b-125">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="3fe6b-125">Remove-AzureRmAutomationWebhook</span></span>

<span data-ttu-id="3fe6b-126">**Batch**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-126">**Batch**</span></span>
- <span data-ttu-id="3fe6b-127">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="3fe6b-127">Remove-AzureBatchCertificate</span></span>
- <span data-ttu-id="3fe6b-128">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3fe6b-128">Remove-AzureBatchComputeNode</span></span>
- <span data-ttu-id="3fe6b-129">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3fe6b-129">Remove-AzureBatchComputeNodeUser</span></span>

<span data-ttu-id="3fe6b-130">**Data factory**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-130">**DataFactories**</span></span>
- <span data-ttu-id="3fe6b-131">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3fe6b-131">Resume-AzureRmDataFactoryPipeline</span></span>
- <span data-ttu-id="3fe6b-132">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="3fe6b-132">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>
- <span data-ttu-id="3fe6b-133">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="3fe6b-133">Suspend-AzureRmDataFactoryPipeline</span></span>

<span data-ttu-id="3fe6b-134">**Data Lake Store**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-134">**DataLakeStore**</span></span>
- <span data-ttu-id="3fe6b-135">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3fe6b-135">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="3fe6b-136">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="3fe6b-136">Set-AzureRmDataLakeStoreItemAcl</span></span>
- <span data-ttu-id="3fe6b-137">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3fe6b-137">Set-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="3fe6b-138">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="3fe6b-138">Set-AzureRmDataLakeStoreItemOwner</span></span>

<span data-ttu-id="3fe6b-139">**Operational Insights**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-139">**OperationalInsights**</span></span>
- <span data-ttu-id="3fe6b-140">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3fe6b-140">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

<span data-ttu-id="3fe6b-141">**Profilo**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-141">**Profile**</span></span>
- <span data-ttu-id="3fe6b-142">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3fe6b-142">Remove-AzureRmEnvironment</span></span>

<span data-ttu-id="3fe6b-143">**RedisCache**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-143">**RedisCache**</span></span>
- <span data-ttu-id="3fe6b-144">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3fe6b-144">Remove-AzureRmRedisCacheDiagnostics</span></span>

<span data-ttu-id="3fe6b-145">**Risorse**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-145">**Resources**</span></span>
- <span data-ttu-id="3fe6b-146">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3fe6b-146">Register-AzureRmProviderFeature</span></span>
- <span data-ttu-id="3fe6b-147">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3fe6b-147">Register-AzureRmResourceProvider</span></span>
- <span data-ttu-id="3fe6b-148">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3fe6b-148">Remove-AzureRmADServicePrincipal</span></span>
- <span data-ttu-id="3fe6b-149">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3fe6b-149">Remove-AzureRmPolicyAssignment</span></span>
- <span data-ttu-id="3fe6b-150">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3fe6b-150">Remove-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="3fe6b-151">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3fe6b-151">Remove-AzureRmRoleAssignment</span></span>
- <span data-ttu-id="3fe6b-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3fe6b-152">Stop-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="3fe6b-153">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3fe6b-153">Unregister-AzureRmResourceProvider</span></span>

<span data-ttu-id="3fe6b-154">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-154">**Storage**</span></span>
- <span data-ttu-id="3fe6b-155">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fe6b-155">Remove-AzureStorageContainerStoredAccessPolicy</span></span>
- <span data-ttu-id="3fe6b-156">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fe6b-156">Remove-AzureStorageQueueStoredAccessPolicy</span></span>
- <span data-ttu-id="3fe6b-157">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fe6b-157">Remove-AzureStorageShareStoredAccessPolicy</span></span>
- <span data-ttu-id="3fe6b-158">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3fe6b-158">Remove-AzureStorageTableStoredAccessPolicy</span></span>

<span data-ttu-id="3fe6b-159">**Analisi di flusso**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-159">**StreamAnalytics**</span></span>
- <span data-ttu-id="3fe6b-160">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3fe6b-160">Remove-AzureRmStreamAnalyticsFunction</span></span>
- <span data-ttu-id="3fe6b-161">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3fe6b-161">Remove-AzureRmStreamAnalyticsInput</span></span>
- <span data-ttu-id="3fe6b-162">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3fe6b-162">Remove-AzureRmStreamAnalyticsJob</span></span>
- <span data-ttu-id="3fe6b-163">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="3fe6b-163">Remove-AzureRmStreamAnalyticsOutput</span></span>

<span data-ttu-id="3fe6b-164">**Tag**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-164">**Tag**</span></span>
- <span data-ttu-id="3fe6b-165">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="3fe6b-165">Remove-AzureRmTag</span></span>

<br>

<span data-ttu-id="3fe6b-166">Se si ha uno script che usa uno dei cmdlet elencati sopra, come correzione per questa modifica di rilievo è sufficiente rimuovere il parametro `Force`.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-166">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by simply removing the `Force` parameter.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a><span data-ttu-id="3fe6b-167">Modifica dei parametri Tag</span><span class="sxs-lookup"><span data-stu-id="3fe6b-167">Change of Tag parameters</span></span>

<span data-ttu-id="3fe6b-168">In questa versione, il nome del parametro `Tags` è stato modificato in `Tag` e il tipo è stato modificato da `Hashtable[]` a `Hashtable`, cambiando il formato delle coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-168">This release, the `Tags` parameter name was changed to `Tag`, and the type was changed from `Hashtable[]` to `Hashtable`, changing the format of the key-value pairings.</span></span>

<span data-ttu-id="3fe6b-169">In precedenza, ogni voce in `Hashtable[]` rappresentava una singola coppia chiave-valore:</span><span class="sxs-lookup"><span data-stu-id="3fe6b-169">Previously, each entry in the `Hashtable[]` represented a single key-value pairing:</span></span>

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

<span data-ttu-id="3fe6b-170">Attualmente non sono più necessari `Name` e `Value` ed è possibile creare coppie chiave-valore assegnando `Key = "Value"` in `Hashtable`:</span><span class="sxs-lookup"><span data-stu-id="3fe6b-170">Now, `Name` and `Value` are no longer necessary, allowing for key-value pairings to be created by assigning `Key = "Value"` in the `Hashtable`:</span></span>

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

<span data-ttu-id="3fe6b-171">I cmdlet interessati da questa modifica sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fe6b-171">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="3fe6b-172">**Batch**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-172">**Batch**</span></span>
- <span data-ttu-id="3fe6b-173">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-173">Get-AzureRmBatchAccount</span></span>
- <span data-ttu-id="3fe6b-174">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-174">New-AzureRmBatchAccount</span></span>
- <span data-ttu-id="3fe6b-175">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-175">Set-AzureRmBatchAccount</span></span>

<span data-ttu-id="3fe6b-176">**Calcolo**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-176">**Compute**</span></span>
- <span data-ttu-id="3fe6b-177">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3fe6b-177">New-AzureRmVM</span></span>
- <span data-ttu-id="3fe6b-178">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3fe6b-178">Update-AzureRmVM</span></span>

<span data-ttu-id="3fe6b-179">**Data Lake Analytics**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-179">**DataLakeAnalytics**</span></span>
- <span data-ttu-id="3fe6b-180">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-180">New-AzureRmDataLakeAnalyticsAccount</span></span>
- <span data-ttu-id="3fe6b-181">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-181">Set-AzureRmDataLakeAnalyticsAccount</span></span>

<span data-ttu-id="3fe6b-182">**Data Lake Store**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-182">**DataLakeStore**</span></span>
- <span data-ttu-id="3fe6b-183">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-183">New-AzureRmDataLakeStoreAccount</span></span>
- <span data-ttu-id="3fe6b-184">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-184">Set-AzureRmDataLakeStoreAccount</span></span>

<span data-ttu-id="3fe6b-185">**DNS**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-185">**Dns**</span></span>
- <span data-ttu-id="3fe6b-186">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3fe6b-186">New-AzureRmDnsZone</span></span>
- <span data-ttu-id="3fe6b-187">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="3fe6b-187">Set-AzureRmDnsZone</span></span>

<span data-ttu-id="3fe6b-188">**Insieme di credenziali delle chiavi**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-188">**KeyVault**</span></span>
- <span data-ttu-id="3fe6b-189">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fe6b-189">Get-AzureRmKeyVault</span></span>
- <span data-ttu-id="3fe6b-190">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fe6b-190">New-AzureRmKeyVault</span></span>

<span data-ttu-id="3fe6b-191">**Rete**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-191">**Network**</span></span>
- <span data-ttu-id="3fe6b-192">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fe6b-192">New-AzureRmApplicationGateway</span></span>
- <span data-ttu-id="3fe6b-193">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3fe6b-193">New-AzureRmExpressRouteCircuit</span></span>
- <span data-ttu-id="3fe6b-194">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3fe6b-194">New-AzureRmLoadBalancer</span></span>
- <span data-ttu-id="3fe6b-195">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3fe6b-195">New-AzureRmLocalNetworkGateway</span></span>
- <span data-ttu-id="3fe6b-196">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3fe6b-196">New-AzureRmNetworkInterface</span></span>
- <span data-ttu-id="3fe6b-197">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3fe6b-197">New-AzureRmNetworkSecurityGroup</span></span>
- <span data-ttu-id="3fe6b-198">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3fe6b-198">New-AzureRmPublicIpAddress</span></span>
- <span data-ttu-id="3fe6b-199">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="3fe6b-199">New-AzureRmRouteTable</span></span>
- <span data-ttu-id="3fe6b-200">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3fe6b-200">New-AzureRmVirtualNetwork</span></span>
- <span data-ttu-id="3fe6b-201">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3fe6b-201">New-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="3fe6b-202">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3fe6b-202">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="3fe6b-203">New-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3fe6b-203">New-AzureRmVirtualNetworkPeering</span></span>

<span data-ttu-id="3fe6b-204">**Risorse**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-204">**Resources**</span></span>
- <span data-ttu-id="3fe6b-205">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3fe6b-205">Find-AzureRmResource</span></span>
- <span data-ttu-id="3fe6b-206">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3fe6b-206">Find-AzureRmResourceGroup</span></span>
- <span data-ttu-id="3fe6b-207">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3fe6b-207">New-AzureRmResource</span></span>
- <span data-ttu-id="3fe6b-208">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3fe6b-208">New-AzureRmResourceGroup</span></span>
- <span data-ttu-id="3fe6b-209">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="3fe6b-209">Set-AzureRmResource</span></span>
- <span data-ttu-id="3fe6b-210">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3fe6b-210">Set-AzureRmResourceGroup</span></span>

<span data-ttu-id="3fe6b-211">**SQL**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-211">**SQL**</span></span>
- <span data-ttu-id="3fe6b-212">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3fe6b-212">New-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="3fe6b-213">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3fe6b-213">New-AzureRmSqlDatabaseCopy</span></span>
- <span data-ttu-id="3fe6b-214">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3fe6b-214">New-AzureRmSqlDatabaseSecondary</span></span>
- <span data-ttu-id="3fe6b-215">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3fe6b-215">New-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="3fe6b-216">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3fe6b-216">New-AzureRmSqlServer</span></span>
- <span data-ttu-id="3fe6b-217">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3fe6b-217">Set-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="3fe6b-218">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3fe6b-218">Set-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="3fe6b-219">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="3fe6b-219">Set-AzureRmSqlServer</span></span>

<span data-ttu-id="3fe6b-220">**Archiviazione**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-220">**Storage**</span></span>
- <span data-ttu-id="3fe6b-221">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-221">New-AzureRmStorageAccount</span></span>
- <span data-ttu-id="3fe6b-222">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fe6b-222">Set-AzureRmStorageAccount</span></span>

<span data-ttu-id="3fe6b-223">**Gestione traffico**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-223">**TrafficManager**</span></span>
- <span data-ttu-id="3fe6b-224">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3fe6b-224">New-AzureRmTrafficManagerProfile</span></span>

<br>

<span data-ttu-id="3fe6b-225">Se si ha uno script che usa uno dei cmdlet elencati sopra, come correzione per questa modifica di rilievo modificare il parametro `Tags` in `Tag` e modificare `Tag` nel nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-225">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by changing the `Tags` parameter to `Tag`, as well as changing the `Tag` to the new format.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="3fe6b-226">Modifiche di rilievo ai cmdlet per Archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fe6b-226">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="3fe6b-227">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fe6b-227">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="3fe6b-228">**Get-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-228">**Get-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="3fe6b-229">Il cmdlet restituisce ora un elenco di chiavi, anziché un oggetto con le proprietà per ogni chiave</span><span class="sxs-lookup"><span data-stu-id="3fe6b-229">The cmdlet now returns a list of keys, rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

<span data-ttu-id="3fe6b-230">**New-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-230">**New-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="3fe6b-231">Il campo `StorageAccountRegenerateKeyResponse` nell'output di questo cmdlet è stato rinominato `StorageAccountListKeysResults`, che è ora un elenco di chiavi anziché un oggetto con le proprietà per ogni chiave</span><span class="sxs-lookup"><span data-stu-id="3fe6b-231">`StorageAccountRegenerateKeyResponse` field in output of this cmdlet is renamed to `StorageAccountListKeysResults`, which is now a list of keys rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

<span data-ttu-id="3fe6b-232">**New/Get/Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-232">**New/Get/Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="3fe6b-233">Il campo `AccountType` nell'output di questo cmdlet è stato rinominato `Sku.Name`</span><span class="sxs-lookup"><span data-stu-id="3fe6b-233">`AccountType` field in output of this cmdlet is renamed to `Sku.Name`</span></span>
- <span data-ttu-id="3fe6b-234">Il tipo di output per BLOB/tabelle/code/file di endpoint primari/secondari è stato modificato da `Uri` a `String`</span><span class="sxs-lookup"><span data-stu-id="3fe6b-234">Output type for PrimaryEndpoints/Secondary endpoints blob/table/queue/file changed from `Uri` to `String`</span></span>

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a><span data-ttu-id="3fe6b-235">Modifiche di rilievo ai cmdlet per AD</span><span class="sxs-lookup"><span data-stu-id="3fe6b-235">Breaking changes to AD cmdlets</span></span>

<span data-ttu-id="3fe6b-236">Questa versione ha interessato i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fe6b-236">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="3fe6b-237">**Get-AzureRMADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-237">**Get-AzureRMADServicePrincipal**</span></span>
- <span data-ttu-id="3fe6b-238">Il campo `ServicePrincipalName` nell'output di questo cmdlet è stato rinominato `ServicePrincipalNames` ed è ora una raccolta.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-238">`ServicePrincipalName` field in output of this cmdlet is renamed to `ServicePrincipalNames` and is now a collection.</span></span> <span data-ttu-id="3fe6b-239">`ApplicationId` viene ora visualizzato come uno dei nomi dell'entità servizio, insieme a identifierUri.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-239">It now displays `ApplicationId` also as one of the SPN, along with the identifierUri.</span></span>

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

<span data-ttu-id="3fe6b-240">**Get-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-240">**Get-AzureRmADApplication**</span></span>
- <span data-ttu-id="3fe6b-241">Il parametro `ApplicationObjectId` è stato rinominato `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-241">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="3fe6b-242">Nell'output di questo cmdlet, `ApplicationObjectId` è stato rinominato `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-242">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

<span data-ttu-id="3fe6b-243">**Remove-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-243">**Remove-AzureRmADApplication**</span></span>
- <span data-ttu-id="3fe6b-244">Il parametro `ApplicationObjectId` è stato rinominato `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-244">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

<span data-ttu-id="3fe6b-245">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-245">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="3fe6b-246">Nell'output di questo cmdlet, `ApplicationObjectId` è stato rinominato `ObjectId`.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-246">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="3fe6b-247">I parametri `KeyValue`, `KeyUsage` e `KeyType` sono stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-247">`KeyValue`, `KeyUsage`, `KeyType` parameters are removed.</span></span>

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

<span data-ttu-id="3fe6b-248">**Get-AzureRmADGroup**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-248">**Get-AzureRmADGroup**</span></span>
- <span data-ttu-id="3fe6b-249">Il campo `Mail` è stato rimosso dall'output.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-249">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="3fe6b-250">**Get-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-250">**Get-AzureRmADUser**</span></span>
- <span data-ttu-id="3fe6b-251">Il campo `Mail` è stato rimosso dall'output.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-251">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="3fe6b-252">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="3fe6b-252">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="3fe6b-253">Rimozione del parametro `DisableAccount`.</span><span class="sxs-lookup"><span data-stu-id="3fe6b-253">Removed `DisableAccount` parameter.</span></span>

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```