## <a name="140---february-2019"></a><span data-ttu-id="c4310-101">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="c4310-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="c4310-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4310-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="c4310-103">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="c4310-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c4310-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c4310-104">Az.Automation</span></span>
* <span data-ttu-id="c4310-105">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="c4310-106">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="c4310-107">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="c4310-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c4310-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="c4310-109">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4310-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-110">Az.Compute</span></span>
* <span data-ttu-id="c4310-111">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="c4310-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="c4310-112">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="c4310-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="c4310-113">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c4310-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="c4310-114">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c4310-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c4310-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="c4310-116">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="c4310-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="c4310-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="c4310-117">Az.EventHub</span></span>
* <span data-ttu-id="c4310-118">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="c4310-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="c4310-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4310-119">Az.KeyVault</span></span>
* <span data-ttu-id="c4310-120">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4310-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c4310-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c4310-121">Az.LogicApp</span></span>
* <span data-ttu-id="c4310-122">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="c4310-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="c4310-123">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="c4310-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="c4310-124">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="c4310-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="c4310-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c4310-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c4310-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c4310-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c4310-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c4310-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="c4310-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="c4310-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="c4310-129">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="c4310-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="c4310-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c4310-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c4310-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="c4310-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="c4310-134">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="c4310-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="c4310-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c4310-135">Az.Monitor</span></span>
* <span data-ttu-id="c4310-136">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="c4310-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c4310-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-137">Az.Network</span></span>
* <span data-ttu-id="c4310-138">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c4310-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="c4310-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c4310-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="c4310-140">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="c4310-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="c4310-141">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c4310-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="c4310-142">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="c4310-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="c4310-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-143">Az.Resources</span></span>
* <span data-ttu-id="c4310-144">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c4310-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c4310-145">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c4310-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="c4310-146">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="c4310-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="c4310-147">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="c4310-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="c4310-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-148">Az.Sql</span></span>
* <span data-ttu-id="c4310-149">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="c4310-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="c4310-150">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="c4310-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c4310-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c4310-151">Az.Websites</span></span>
* <span data-ttu-id="c4310-152">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="c4310-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="c4310-153">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="c4310-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c4310-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-154">Az.Accounts</span></span>
* <span data-ttu-id="c4310-155">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c4310-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c4310-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4310-156">Az.AnalysisServices</span></span>
<span data-ttu-id="c4310-157">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="c4310-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-158">Az.Compute</span></span>
* <span data-ttu-id="c4310-159">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="c4310-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="c4310-160">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c4310-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="c4310-161">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="c4310-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c4310-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c4310-162">Az.RecoveryServices</span></span>
<span data-ttu-id="c4310-163">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="c4310-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c4310-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-164">Az.Resources</span></span>
* <span data-ttu-id="c4310-165">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="c4310-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="c4310-166">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="c4310-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="c4310-167">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="c4310-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="c4310-168">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="c4310-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="c4310-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-169">Az.Sql</span></span>
* <span data-ttu-id="c4310-170">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c4310-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="c4310-171">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="c4310-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="c4310-172">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="c4310-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="c4310-173">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="c4310-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c4310-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-174">Az.Accounts</span></span>
* <span data-ttu-id="c4310-175">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="c4310-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="c4310-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4310-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="c4310-177">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="c4310-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="c4310-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c4310-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="c4310-179">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="c4310-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="c4310-180">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="c4310-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c4310-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-181">Az.Accounts</span></span>
* <span data-ttu-id="c4310-182">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="c4310-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="c4310-183">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c4310-184">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="c4310-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="c4310-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="c4310-185">Az.Aks</span></span>
* <span data-ttu-id="c4310-186">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="c4310-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c4310-187">Az.Automation</span></span>
* <span data-ttu-id="c4310-188">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="c4310-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="c4310-189">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="c4310-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="c4310-190">Az.Cdn</span></span>
* <span data-ttu-id="c4310-191">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-192">Az.Compute</span></span>
* <span data-ttu-id="c4310-193">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="c4310-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="c4310-194">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c4310-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="c4310-195">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c4310-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="c4310-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c4310-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="c4310-197">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="c4310-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="c4310-198">Az.DataFactory</span></span>
* <span data-ttu-id="c4310-199">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="c4310-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c4310-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="c4310-201">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="c4310-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="c4310-202">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="c4310-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="c4310-203">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c4310-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c4310-204">Az.IotHub</span></span>
* <span data-ttu-id="c4310-205">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c4310-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="c4310-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4310-206">Az.KeyVault</span></span>
* <span data-ttu-id="c4310-207">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c4310-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-208">Az.Network</span></span>
* <span data-ttu-id="c4310-209">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="c4310-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-210">Az.Resources</span></span>
* <span data-ttu-id="c4310-211">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="c4310-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="c4310-212">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c4310-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="c4310-213">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="c4310-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="c4310-214">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="c4310-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="c4310-215">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="c4310-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="c4310-216">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="c4310-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="c4310-217">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="c4310-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c4310-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4310-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="c4310-219">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="c4310-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="c4310-220">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="c4310-220">Fix some error messages.</span></span>
* <span data-ttu-id="c4310-221">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="c4310-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="c4310-222">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="c4310-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c4310-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c4310-223">Az.SignalR</span></span>
* <span data-ttu-id="c4310-224">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="c4310-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-225">Az.Sql</span></span>
* <span data-ttu-id="c4310-226">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c4310-227">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="c4310-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="c4310-228">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="c4310-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="c4310-229">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="c4310-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c4310-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c4310-230">Az.Storage</span></span>
* <span data-ttu-id="c4310-231">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c4310-232">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="c4310-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="c4310-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c4310-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="c4310-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="c4310-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="c4310-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4310-235">Az.TrafficManager</span></span>
* <span data-ttu-id="c4310-236">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c4310-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c4310-237">Az.Websites</span></span>
* <span data-ttu-id="c4310-238">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="c4310-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="c4310-239">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4310-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="c4310-240">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="c4310-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="c4310-241">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="c4310-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="c4310-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-242">Az.Accounts</span></span>
* <span data-ttu-id="c4310-243">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="c4310-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-244">Az.Compute</span></span>
* <span data-ttu-id="c4310-245">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c4310-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="c4310-246">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="c4310-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="c4310-247">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c4310-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="c4310-249">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="c4310-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="c4310-250">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="c4310-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="c4310-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c4310-251">Az.EventGrid</span></span>
* <span data-ttu-id="c4310-252">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="c4310-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="c4310-253">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="c4310-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="c4310-254">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="c4310-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c4310-255">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="c4310-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c4310-256">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="c4310-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c4310-257">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="c4310-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="c4310-258">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="c4310-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="c4310-259">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="c4310-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="c4310-260">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="c4310-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="c4310-261">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="c4310-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="c4310-262">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="c4310-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="c4310-263">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c4310-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="c4310-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="c4310-264">Az.IotHub</span></span>
* <span data-ttu-id="c4310-265">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="c4310-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="c4310-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c4310-266">Az.LogicApp</span></span>
* <span data-ttu-id="c4310-267">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="c4310-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="c4310-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-268">Az.Resources</span></span>
* <span data-ttu-id="c4310-269">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="c4310-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="c4310-270">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="c4310-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="c4310-271">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c4310-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c4310-272">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c4310-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="c4310-273">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="c4310-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="c4310-274">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="c4310-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="c4310-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="c4310-275">Az.SignalR</span></span>
* <span data-ttu-id="c4310-276">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="c4310-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-277">Az.Sql</span></span>
* <span data-ttu-id="c4310-278">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="c4310-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="c4310-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c4310-279">Az.Storage</span></span>
* <span data-ttu-id="c4310-280">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="c4310-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="c4310-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c4310-281">New-AzStorageContext</span></span>
* <span data-ttu-id="c4310-282">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="c4310-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="c4310-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c4310-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c4310-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c4310-284">Az.Websites</span></span>
* <span data-ttu-id="c4310-285">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="c4310-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="c4310-286">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="c4310-287">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c4310-288">Generale</span><span class="sxs-lookup"><span data-stu-id="c4310-288">General</span></span>

- <span data-ttu-id="c4310-289">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="c4310-289">General Availability of Az Module</span></span>
- <span data-ttu-id="c4310-290">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="c4310-290">Online help for each module</span></span>
- <span data-ttu-id="c4310-291">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c4310-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c4310-292">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="c4310-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c4310-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-293">Az.Accounts</span></span>
- <span data-ttu-id="c4310-294">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c4310-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="c4310-295">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="c4310-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c4310-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4310-296">Az.ApiManagement</span></span>
- <span data-ttu-id="c4310-297">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="c4310-297">Fixes for #7002</span></span>
- <span data-ttu-id="c4310-298">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c4310-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c4310-299">Az.Batch</span></span>
- <span data-ttu-id="c4310-300">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="c4310-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c4310-301">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="c4310-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c4310-302">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c4310-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c4310-303">Az.Billing</span></span>
- <span data-ttu-id="c4310-304">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c4310-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c4310-305">Az.CognitivServices</span></span>
- <span data-ttu-id="c4310-306">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c4310-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c4310-307">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="c4310-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c4310-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c4310-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="c4310-309">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="c4310-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c4310-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c4310-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c4310-311">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c4310-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="c4310-313">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c4310-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c4310-314">Az.Monitor</span></span>
- <span data-ttu-id="c4310-315">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c4310-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4310-316">Az.KeyVault</span></span>
- <span data-ttu-id="c4310-317">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="c4310-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c4310-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c4310-318">Az.MachineLearning</span></span>
- <span data-ttu-id="c4310-319">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c4310-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c4310-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c4310-320">Az.Media</span></span>
- <span data-ttu-id="c4310-321">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c4310-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c4310-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-322">Az.Network</span></span>
<span data-ttu-id="c4310-323">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c4310-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c4310-324">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="c4310-324">New cmdlets added:</span></span>
        - <span data-ttu-id="c4310-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4310-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c4310-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4310-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c4310-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4310-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c4310-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4310-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c4310-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4310-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c4310-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c4310-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c4310-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c4310-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c4310-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4310-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c4310-333">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4310-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c4310-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4310-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c4310-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4310-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c4310-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4310-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c4310-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4310-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c4310-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c4310-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c4310-339">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="c4310-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c4310-340">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4310-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c4310-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c4310-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c4310-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c4310-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c4310-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c4310-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c4310-344">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="c4310-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c4310-345">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c4310-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c4310-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="c4310-347">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c4310-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c4310-348">Az.Profile</span></span>
- <span data-ttu-id="c4310-349">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c4310-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c4310-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c4310-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="c4310-351">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c4310-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-352">Az.Resources</span></span>
- <span data-ttu-id="c4310-353">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c4310-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4310-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="c4310-355">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="c4310-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c4310-356">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c4310-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c4310-357">Az.SIgnalR</span></span>
- <span data-ttu-id="c4310-358">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c4310-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c4310-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-359">Az.Sql</span></span>
- <span data-ttu-id="c4310-360">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="c4310-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c4310-361">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c4310-362">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c4310-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c4310-363">Az.Storage</span></span>
- <span data-ttu-id="c4310-364">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c4310-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c4310-365">Az.Websites</span></span>
- <span data-ttu-id="c4310-366">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c4310-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c4310-367">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c4310-368">Generale</span><span class="sxs-lookup"><span data-stu-id="c4310-368">General</span></span>

* <span data-ttu-id="c4310-369">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="c4310-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c4310-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-370">Az.Compute</span></span>

* <span data-ttu-id="c4310-371">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="c4310-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c4310-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="c4310-373">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="c4310-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c4310-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c4310-374">Az.FrontDoor</span></span>

* <span data-ttu-id="c4310-375">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="c4310-375">Fixed some broken links</span></span>
    - <span data-ttu-id="c4310-376">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="c4310-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c4310-377">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="c4310-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c4310-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c4310-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="c4310-379">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4310-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c4310-380">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="c4310-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c4310-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-381">Az.Resources</span></span>

* <span data-ttu-id="c4310-382">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="c4310-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c4310-383">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="c4310-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c4310-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-384">Az.Sql</span></span>

* <span data-ttu-id="c4310-385">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="c4310-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c4310-386">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="c4310-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c4310-387">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="c4310-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c4310-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c4310-388">Az.Storage</span></span>

* <span data-ttu-id="c4310-389">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4310-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c4310-390">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="c4310-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c4310-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c4310-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c4310-392">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="c4310-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="c4310-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c4310-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c4310-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c4310-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c4310-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c4310-395">Az.Websites</span></span>

* <span data-ttu-id="c4310-396">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c4310-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c4310-397">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="c4310-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c4310-398">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4310-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c4310-399">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c4310-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4310-400">Az.ApiManagement</span></span>
* <span data-ttu-id="c4310-401">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4310-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c4310-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c4310-402">Az.Automation</span></span>
* <span data-ttu-id="c4310-403">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="c4310-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c4310-404">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="c4310-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c4310-405">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="c4310-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c4310-406">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c4310-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c4310-407">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="c4310-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c4310-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-408">Az.Compute</span></span>
* <span data-ttu-id="c4310-409">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c4310-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c4310-410">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4310-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c4310-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c4310-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="c4310-412">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4310-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c4310-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c4310-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c4310-414">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="c4310-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c4310-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-415">Az.Network</span></span>
* <span data-ttu-id="c4310-416">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c4310-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c4310-417">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="c4310-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c4310-418">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c4310-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c4310-419">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4310-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c4310-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c4310-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c4310-421">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="c4310-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c4310-422">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="c4310-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c4310-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c4310-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c4310-424">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c4310-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c4310-425">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4310-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c4310-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c4310-426">Az.Relay</span></span>
* <span data-ttu-id="c4310-427">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c4310-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c4310-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-428">Az.Resources</span></span>
* <span data-ttu-id="c4310-429">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="c4310-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c4310-430">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="c4310-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c4310-431">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c4310-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c4310-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4310-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="c4310-433">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="c4310-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c4310-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-434">Az.Sql</span></span>
* <span data-ttu-id="c4310-435">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="c4310-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c4310-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c4310-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c4310-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c4310-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c4310-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c4310-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c4310-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c4310-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c4310-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c4310-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c4310-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c4310-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c4310-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c4310-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c4310-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c4310-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c4310-444">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="c4310-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c4310-445">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="c4310-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c4310-446">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="c4310-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c4310-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c4310-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c4310-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c4310-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c4310-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c4310-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c4310-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c4310-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c4310-451">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c4310-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c4310-452">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c4310-453">Generale</span><span class="sxs-lookup"><span data-stu-id="c4310-453">General</span></span>
* <span data-ttu-id="c4310-454">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="c4310-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c4310-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c4310-455">Az.Profile</span></span>
* <span data-ttu-id="c4310-456">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c4310-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c4310-457">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="c4310-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c4310-458">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="c4310-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c4310-459">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="c4310-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c4310-460">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="c4310-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c4310-461">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="c4310-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c4310-462">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="c4310-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c4310-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c4310-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="c4310-464">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="c4310-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-465">Az.Compute</span></span>
* <span data-ttu-id="c4310-466">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c4310-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c4310-467">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c4310-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c4310-468">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="c4310-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c4310-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="c4310-470">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="c4310-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c4310-471">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="c4310-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c4310-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c4310-472">Az.Insights</span></span>
* <span data-ttu-id="c4310-473">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="c4310-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c4310-474">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="c4310-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c4310-475">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="c4310-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c4310-476">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="c4310-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c4310-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-477">Az.Network</span></span>
* <span data-ttu-id="c4310-478">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4310-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c4310-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c4310-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c4310-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c4310-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c4310-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c4310-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c4310-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c4310-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c4310-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c4310-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c4310-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c4310-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c4310-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c4310-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="c4310-486">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="c4310-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c4310-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-487">Az.Resources</span></span>
* <span data-ttu-id="c4310-488">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c4310-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c4310-489">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="c4310-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c4310-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4310-490">Az.ServiceBus</span></span>
* <span data-ttu-id="c4310-491">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="c4310-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c4310-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4310-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="c4310-493">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="c4310-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c4310-494">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="c4310-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c4310-495">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c4310-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c4310-496">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c4310-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c4310-497">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="c4310-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c4310-498">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c4310-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c4310-499">Az.Profile</span></span>
* <span data-ttu-id="c4310-500">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="c4310-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c4310-501">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c4310-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-502">Az.Compute</span></span>
* <span data-ttu-id="c4310-503">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="c4310-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c4310-504">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4310-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c4310-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4310-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="c4310-506">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c4310-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c4310-507">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4310-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c4310-508">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c4310-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c4310-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c4310-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c4310-510">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c4310-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c4310-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-511">Az.Network</span></span>
* <span data-ttu-id="c4310-512">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="c4310-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c4310-513">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4310-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c4310-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-514">Az.Resources</span></span>
* <span data-ttu-id="c4310-515">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="c4310-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c4310-516">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="c4310-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c4310-517">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c4310-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c4310-518">Azure.Storage</span></span>
* <span data-ttu-id="c4310-519">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="c4310-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c4310-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c4310-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c4310-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c4310-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c4310-522">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="c4310-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c4310-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c4310-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c4310-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c4310-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="c4310-525">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="c4310-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c4310-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c4310-526">Az.Compute</span></span>
* <span data-ttu-id="c4310-527">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="c4310-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c4310-528">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="c4310-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c4310-529">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="c4310-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c4310-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c4310-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c4310-531">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="c4310-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c4310-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c4310-532">Az.Network</span></span>
* <span data-ttu-id="c4310-533">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c4310-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c4310-534">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4310-534">new cmdlets added</span></span>
    - <span data-ttu-id="c4310-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c4310-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c4310-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c4310-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c4310-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c4310-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c4310-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c4310-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c4310-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c4310-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c4310-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4310-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c4310-541">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="c4310-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c4310-542">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c4310-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c4310-543">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c4310-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c4310-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c4310-544">Az.RedisCache</span></span>
* <span data-ttu-id="c4310-545">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="c4310-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c4310-546">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="c4310-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c4310-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c4310-547">Az.Resources</span></span>
* <span data-ttu-id="c4310-548">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c4310-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c4310-549">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="c4310-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c4310-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c4310-550">Az.Sql</span></span>
* <span data-ttu-id="c4310-551">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="c4310-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c4310-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c4310-552">Az.Websites</span></span>
* <span data-ttu-id="c4310-553">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="c4310-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c4310-554">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c4310-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c4310-555">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="c4310-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c4310-556">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="c4310-556">Initial Release</span></span>