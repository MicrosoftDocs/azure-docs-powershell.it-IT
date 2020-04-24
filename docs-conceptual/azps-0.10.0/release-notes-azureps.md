---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: c02cfaa7f7f39393f21cec31c5115f009381b19c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "81446054"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="8ecf2-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ecf2-103">Azure PowerShell release notes</span></span>
## <a name="0100-preview---april-2020"></a><span data-ttu-id="8ecf2-104">0.10.0-preview - Aprile 2020</span><span class="sxs-lookup"><span data-stu-id="8ecf2-104">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="8ecf2-105">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-105">General</span></span>
* <span data-ttu-id="8ecf2-106">Disponibilità di moduli Az in anteprima nell'hub di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-106">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="8ecf2-107">Consentono la compatibilità multipiattaforma con Linux e macOS.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-107">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="8ecf2-108">L'hub di Azure Stack ora supporta PowerShell core con i moduli Az. Per altre informazioni, vedere [qui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-108">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="8ecf2-109">I moduli Az supportano il profilo 2019-03-01-ibrido:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-109">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="8ecf2-110">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8ecf2-110">Az.Billing</span></span>
  - <span data-ttu-id="8ecf2-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-111">Az.Compute</span></span>
  - <span data-ttu-id="8ecf2-112">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-112">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="8ecf2-113">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-113">Az.EventHub</span></span>
  - <span data-ttu-id="8ecf2-114">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-114">Az.IotHub</span></span>
  - <span data-ttu-id="8ecf2-115">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-115">Az.KeyVault</span></span>
  - <span data-ttu-id="8ecf2-116">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-116">Az.Monitor</span></span>
  - <span data-ttu-id="8ecf2-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-117">Az.Network</span></span>
  - <span data-ttu-id="8ecf2-118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-118">Az.Resources</span></span>
  - <span data-ttu-id="8ecf2-119">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-119">Az.Storage</span></span>
  - <span data-ttu-id="8ecf2-120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-120">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-121">Sono stati introdotti tre nuovi moduli di PowerShell per az compatibili con l'hub di Azure Stack, ovvero Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-121">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-122">I comandi rimangono relativamente invariati, con modifiche minime come la sostituzione di AzureRM con Az</span><span class="sxs-lookup"><span data-stu-id="8ecf2-122">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="8ecf2-123">Il collegamento aggiornato alla documentazione di PowerShell per l'hub di Azure Stack è reperibile [qui](aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-123">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](aka.ms/InstallASHPowerShell)</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-124">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-125">Aggiornamento da ADAL a MSAL</span><span class="sxs-lookup"><span data-stu-id="8ecf2-125">Upgrade from ADAL to MSAL</span></span>


## <a name="370---march-2020"></a><span data-ttu-id="8ecf2-126">3.7.0 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="8ecf2-126">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-127">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-127">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-128">Correzione dell'eccezione NullReferenceException generata da 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' in caso di mancato accesso [#10292]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-128">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-129">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-129">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-130">Aggiunta dei parametri seguenti al cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="8ecf2-130">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="8ecf2-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="8ecf2-131">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="8ecf2-132">Proprietà Encryption consentita per il parametro Target del cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-132">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="8ecf2-133">Correzione del problema tempDisk per i cmdlet 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-133">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="8ecf2-134">[#11354]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-134">[#11354]</span></span>
* <span data-ttu-id="8ecf2-135">Aggiunta del supporto dei cmdlet seguenti per la nuova estensione SAP</span><span class="sxs-lookup"><span data-stu-id="8ecf2-135">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="8ecf2-136">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-136">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8ecf2-137">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-137">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8ecf2-138">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-138">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="8ecf2-139">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-139">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="8ecf2-140">Correzione di errori negli esempi del documento della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-140">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="8ecf2-141">Visualizzazione del valore stringa esatto per PowerState VM nel formato tabella.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-141">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="8ecf2-142">'New-AzVmssConfig': correzione della serializzazione della proprietà AutomaticRepairs quando SinglePlacementGroup è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-142">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="8ecf2-143">[#11257]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-143">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-144">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-144">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-145">Aggiornamento di ADF .NET SDK alla versione 4.8.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-145">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="8ecf2-146">Aggiunta di parametri facoltativi al comando 'Invoke-AzDataFactoryV2Pipeline' per supportare la riesecuzione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-146">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-147">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-147">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-148">Aggiunta della descrizione della modifica di rilievo per 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-148">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="8ecf2-149">Aggiunta dell'opzione di codifica Byte per 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-149">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-150">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-150">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-151">Supporto della versione minima supportata di TLS durante la creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-151">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-152">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-152">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-153">Aggiunta del supporto per gestire le impostazioni distribuite per singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-153">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="8ecf2-154">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-154">New Cmdlets are:</span></span>
    - <span data-ttu-id="8ecf2-155">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-155">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="8ecf2-156">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-156">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-157">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-157">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-158">Aggiunta degli attributi della modifica di rilievo a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-158">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-159">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-159">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-160">Documentazione aggiornata per 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-160">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-161">Az.Network</span></span>
* <span data-ttu-id="8ecf2-162">Aggiornamento dei cmdlet per consentire VirtualHubVnetConnections tra tenant</span><span class="sxs-lookup"><span data-stu-id="8ecf2-162">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="8ecf2-163">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-163">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8ecf2-164">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-164">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="8ecf2-165">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-165">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="8ecf2-166">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-166">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="8ecf2-167">Rimozione della dipendenza di SQL Management SDK</span><span class="sxs-lookup"><span data-stu-id="8ecf2-167">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ecf2-168">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-168">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ecf2-169">Miglioramento dei messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-169">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-170">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-171">Azure Site Recovery: aggiunto il supporto per la riprotezione e aggiornamento delle proprietà delle VM per le macchine virtuali con crittografia dischi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-171">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="8ecf2-172">Azure Site Recovery: aggiunta del monitoraggio per il ripristino di emergenza nelle proprietà VmwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-172">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="8ecf2-173">Backup di Azure: aggiunta del supporto per la ripetizione dell'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-173">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="8ecf2-174">Backup di Azure: aggiunta del supporto per le impostazioni di esclusione disco durante il backup e il ripristino.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-174">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="8ecf2-175">Backup di Azure: aggiunta del supporto per il ripristino di più file/cartelle in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-175">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="8ecf2-176">Backup di Azure: aggiunta del supporto per il gruppo di risorse specificato dall'utente durante l'aggiornamento dei criteri IaasVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-176">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-177">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-178">Correzione di 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' per l'utilizzo del valore effettivo di apiVersion per le risorse invece di quello predefinito [#11267]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-178">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="8ecf2-179">Aggiunta della registrazione di correlationId per gli scenari di errore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-179">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="8ecf2-180">Modifica di lieve entità alla documentazione di 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-180">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="8ecf2-181">Aggiunta dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-181">Added example.</span></span>
* <span data-ttu-id="8ecf2-182">Aggiunta della virgoletta singola come carattere di escape nel valore di parametro 'Get-AzADUser' [#11317]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-182">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="8ecf2-183">Aggiunta di nuovi cmdlet per gli script di distribuzione ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="8ecf2-183">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-184">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-185">Aggiunta del parametro secondario leggibile a 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-185">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="8ecf2-186">Aggiunta del cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-186">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="8ecf2-187">Salvataggio della classificazione di riservatezza durante la classificazione delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-187">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="8ecf2-188">Az.Support</span><span class="sxs-lookup"><span data-stu-id="8ecf2-188">Az.Support</span></span>
* <span data-ttu-id="8ecf2-189">Disponibilità generale del modulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-189">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-190">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-190">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-191">Aggiunta del supporto per l'uso delle regole di gestione del traffico delle app Web con i nuovi cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-191">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="8ecf2-192">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-192">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8ecf2-193">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-193">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8ecf2-194">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-194">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="8ecf2-195">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-195">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="8ecf2-196">3.6.1 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="8ecf2-196">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-197">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-198">Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-198">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="8ecf2-199">Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-199">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="8ecf2-200">Aggiunta la versione Az in UserAgent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-200">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-201">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-202">Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-202">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="8ecf2-203">'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-203">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="8ecf2-204">'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON</span><span class="sxs-lookup"><span data-stu-id="8ecf2-204">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="8ecf2-205">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-205">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-206">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-206">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-207">Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-207">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-208">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-209">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-209">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8ecf2-210">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-210">New Cmdlets are:</span></span>
    - <span data-ttu-id="8ecf2-211">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-211">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8ecf2-212">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-212">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8ecf2-213">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-213">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8ecf2-214">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-214">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="8ecf2-215">Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-215">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="8ecf2-216">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-216">New Cmdlets are:</span></span>
    - <span data-ttu-id="8ecf2-217">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-217">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="8ecf2-218">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-218">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="8ecf2-219">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-219">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="8ecf2-220">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-220">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="8ecf2-221">Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-221">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8ecf2-222">Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-222">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="8ecf2-223">Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-223">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="8ecf2-224">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-224">New Cmdlets are:</span></span>
    - <span data-ttu-id="8ecf2-225">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-225">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="8ecf2-226">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-226">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="8ecf2-227">Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-227">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-228">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-228">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-229">Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-229">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-230">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-230">Az.Network</span></span>
* <span data-ttu-id="8ecf2-231">Aggiornamento di SQL Management SDK.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-231">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="8ecf2-232">Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-232">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="8ecf2-233">Mapping del campo ActionsRequired a ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-233">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="8ecf2-234">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-234">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-235">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-235">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-236">Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-236">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="8ecf2-237">Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-237">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="8ecf2-238">Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-238">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="8ecf2-239">Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-239">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="8ecf2-240">Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="8ecf2-240">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="8ecf2-241">Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri</span><span class="sxs-lookup"><span data-stu-id="8ecf2-241">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="8ecf2-242">Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server</span><span class="sxs-lookup"><span data-stu-id="8ecf2-242">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="8ecf2-243">Estensione dei cmdlet Tag per l'accettazione di -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-243">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="8ecf2-244">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-244">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8ecf2-245">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-245">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="8ecf2-246">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-246">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="8ecf2-247">Aggiunta di nuovi cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="8ecf2-247">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="8ecf2-248">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-248">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="8ecf2-249">Inclusione di ScopedDeployment da SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-249">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-250">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-251">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-251">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="8ecf2-252">Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-252">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="8ecf2-253">Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito</span><span class="sxs-lookup"><span data-stu-id="8ecf2-253">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="8ecf2-254">Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-254">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="8ecf2-255">Rimozione di un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="8ecf2-255">Remove an LTR backup</span></span>
    - <span data-ttu-id="8ecf2-256">Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito</span><span class="sxs-lookup"><span data-stu-id="8ecf2-256">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="8ecf2-257">Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="8ecf2-257">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="8ecf2-258">Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-258">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="8ecf2-259">Bump della versione di SQL SDK per Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-259">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-260">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-261">Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-261">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="8ecf2-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-262">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="8ecf2-263">Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura</span><span class="sxs-lookup"><span data-stu-id="8ecf2-263">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="8ecf2-264">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-264">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="8ecf2-265">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-265">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-266">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-267">Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-267">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="8ecf2-268">Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web</span><span class="sxs-lookup"><span data-stu-id="8ecf2-268">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="8ecf2-269">Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="8ecf2-269">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="8ecf2-270">Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-270">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="8ecf2-271">Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="8ecf2-271">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="8ecf2-272">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="8ecf2-272">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ecf2-273">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-273">Highlights since the last major release</span></span>
* <span data-ttu-id="8ecf2-274">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-274">Updated client side telemetry.</span></span>
* <span data-ttu-id="8ecf2-275">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-275">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="8ecf2-276">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-276">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-277">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-278">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="8ecf2-278">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-279">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-279">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-280">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-280">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-281">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-282">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-282">Updated SDK to 7.0</span></span>
* <span data-ttu-id="8ecf2-283">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-283">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-284">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-284">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-285">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8ecf2-285">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-286">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-286">Az.FrontDoor</span></span>
* <span data-ttu-id="8ecf2-287">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="8ecf2-287">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-288">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-288">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-289">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-289">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="8ecf2-290">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-290">New Cmdlets are:</span></span>
    - <span data-ttu-id="8ecf2-291">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-291">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8ecf2-292">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-292">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8ecf2-293">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-293">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="8ecf2-294">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-294">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-295">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-295">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-296">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="8ecf2-296">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-297">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-297">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-298">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-298">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="8ecf2-299">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-299">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="8ecf2-300">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-300">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-301">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-301">Az.Network</span></span>
* <span data-ttu-id="8ecf2-302">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-302">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="8ecf2-303">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-303">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8ecf2-304">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-304">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="8ecf2-305">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-305">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="8ecf2-306">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-306">No new cmdlets are added.</span></span> <span data-ttu-id="8ecf2-307">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-307">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-308">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-309">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-309">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-310">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-310">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-311">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="8ecf2-311">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="8ecf2-312">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-312">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="8ecf2-313">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-313">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="8ecf2-314">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-314">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="8ecf2-315">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-315">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="8ecf2-316">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-316">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="8ecf2-317">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-317">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="8ecf2-318">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-318">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-319">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-320">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-320">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="8ecf2-321">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="8ecf2-321">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="8ecf2-322">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="8ecf2-322">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8ecf2-323">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8ecf2-323">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8ecf2-324">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="8ecf2-324">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8ecf2-325">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8ecf2-325">Az.StorageSync</span></span>
* <span data-ttu-id="8ecf2-326">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-326">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="8ecf2-327">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="8ecf2-327">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ecf2-328">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-328">Highlights since the last major release</span></span>
* <span data-ttu-id="8ecf2-329">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8ecf2-329">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="8ecf2-330">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-330">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-331">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-332">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-332">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="8ecf2-333">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="8ecf2-333">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-334">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-334">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-335">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="8ecf2-335">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="8ecf2-336">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-336">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="8ecf2-337">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="8ecf2-337">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="8ecf2-338">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-338">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-339">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-340">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-340">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="8ecf2-341">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-341">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="8ecf2-342">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-342">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="8ecf2-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-343">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="8ecf2-344">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-344">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-345">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-346">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-346">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8ecf2-347">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8ecf2-347">Az.DeploymentManager</span></span>
* <span data-ttu-id="8ecf2-348">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="8ecf2-348">Adds LIST operations for resources</span></span>
* <span data-ttu-id="8ecf2-349">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="8ecf2-349">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-350">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-351">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-351">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-352">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-353">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-353">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-354">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-354">Az.Network</span></span>
* <span data-ttu-id="8ecf2-355">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-355">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="8ecf2-356">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-356">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="8ecf2-357">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-357">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-358">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-358">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="8ecf2-359">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-359">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="8ecf2-360">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-360">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="8ecf2-361">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-361">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="8ecf2-362">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-362">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="8ecf2-363">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-363">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-364">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="8ecf2-365">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-365">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="8ecf2-366">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-366">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="8ecf2-367">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-367">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ecf2-368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-368">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ecf2-369">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="8ecf2-369">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="8ecf2-370">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-370">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="8ecf2-371">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="8ecf2-371">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="8ecf2-372">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="8ecf2-372">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-373">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-373">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-374">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-374">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="8ecf2-375">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-375">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-376">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-377">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="8ecf2-377">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="8ecf2-378">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="8ecf2-378">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-379">Az.Sql</span></span>
<span data-ttu-id="8ecf2-380">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-380">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-381">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-381">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-382">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-382">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="8ecf2-383">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-383">New-AzStorageAccount</span></span>
* <span data-ttu-id="8ecf2-384">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-384">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="8ecf2-385">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-385">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-386">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-386">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-387">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="8ecf2-387">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="8ecf2-388">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-388">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="8ecf2-389">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="8ecf2-389">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-390">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-390">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-391">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8ecf2-391">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ecf2-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-392">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-393">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ecf2-393">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-394">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-395">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-395">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8ecf2-396">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-396">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ecf2-397">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-397">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8ecf2-398">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-398">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8ecf2-399">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-399">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8ecf2-400">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-400">Get the Edge Storage Container</span></span>
* <span data-ttu-id="8ecf2-401">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-401">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8ecf2-402">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-402">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="8ecf2-403">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-403">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8ecf2-404">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-404">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="8ecf2-405">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-405">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="8ecf2-406">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-406">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="8ecf2-407">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-407">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8ecf2-408">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-408">Get the Edge Storage Account</span></span>
* <span data-ttu-id="8ecf2-409">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-409">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8ecf2-410">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-410">Create new Edge Storage Account</span></span>
* <span data-ttu-id="8ecf2-411">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-411">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="8ecf2-412">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-412">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="8ecf2-413">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-413">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="8ecf2-414">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-414">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="8ecf2-415">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-415">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="8ecf2-416">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-416">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-417">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-417">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-418">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8ecf2-418">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="8ecf2-419">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-419">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="8ecf2-420">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-420">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="8ecf2-421">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8ecf2-421">Az.DevTestLabs</span></span>
* <span data-ttu-id="8ecf2-422">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="8ecf2-422">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-423">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-423">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-424">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="8ecf2-424">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-425">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-425">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-426">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-426">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8ecf2-427">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ecf2-427">Az.MachineLearning</span></span>
* <span data-ttu-id="8ecf2-428">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-428">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="8ecf2-429">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8ecf2-429">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="8ecf2-430">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-430">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="8ecf2-431">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8ecf2-431">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="8ecf2-432">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8ecf2-432">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="8ecf2-433">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8ecf2-433">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="8ecf2-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="8ecf2-434">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="8ecf2-435">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-435">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-436">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-436">Az.Network</span></span>
* <span data-ttu-id="8ecf2-437">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="8ecf2-437">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-439">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-439">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="8ecf2-440">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-440">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8ecf2-441">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-441">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="8ecf2-442">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-442">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-443">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-444">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-444">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-445">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-446">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-446">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="8ecf2-447">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="8ecf2-447">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="8ecf2-448">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8ecf2-448">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="8ecf2-449">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="8ecf2-449">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-450">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-450">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-451">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="8ecf2-451">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="8ecf2-452">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-452">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="8ecf2-453">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="8ecf2-453">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="8ecf2-454">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-454">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="8ecf2-455">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-455">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="8ecf2-456">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-456">General</span></span>
* <span data-ttu-id="8ecf2-457">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="8ecf2-457">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-458">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-459">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-459">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="8ecf2-460">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-460">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ecf2-461">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-461">Az.Batch</span></span>
* <span data-ttu-id="8ecf2-462">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-462">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-463">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-463">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-464">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-464">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-465">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-465">Az.FrontDoor</span></span>
* <span data-ttu-id="8ecf2-466">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="8ecf2-466">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="8ecf2-467">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-467">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8ecf2-468">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8ecf2-468">Az.HealthcareApis</span></span>
* <span data-ttu-id="8ecf2-469">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="8ecf2-469">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-470">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-470">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-471">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-471">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="8ecf2-472">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-472">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="8ecf2-473">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-473">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-474">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-475">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-475">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="8ecf2-476">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="8ecf2-476">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="8ecf2-477">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-477">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-478">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-478">Az.Network</span></span>
* <span data-ttu-id="8ecf2-479">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-479">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-480">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-480">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-481">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-481">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="8ecf2-482">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-482">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-483">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-484">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="8ecf2-484">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-485">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-485">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-486">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="8ecf2-486">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="8ecf2-487">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="8ecf2-487">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="8ecf2-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8ecf2-488">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="8ecf2-489">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="8ecf2-489">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="8ecf2-490">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="8ecf2-490">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="8ecf2-491">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-491">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="8ecf2-492">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-492">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="8ecf2-493">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-493">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="8ecf2-494">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-494">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="8ecf2-495">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-495">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="8ecf2-496">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8ecf2-496">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="8ecf2-497">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-497">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="8ecf2-498">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="8ecf2-498">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="8ecf2-499">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-499">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ecf2-500">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-500">Highlights since the last major release</span></span>
* <span data-ttu-id="8ecf2-501">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-501">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="8ecf2-502">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-502">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-503">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-503">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-504">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-504">VM Reapply feature</span></span>
    - <span data-ttu-id="8ecf2-505">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-505">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="8ecf2-506">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-506">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="8ecf2-507">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-507">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="8ecf2-508">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-508">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="8ecf2-509">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-509">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8ecf2-510">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="8ecf2-510">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="8ecf2-511">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-511">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="8ecf2-512">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8ecf2-512">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="8ecf2-513">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="8ecf2-513">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="8ecf2-514">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-514">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="8ecf2-515">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="8ecf2-515">Az.DataBoxEdge</span></span>
* <span data-ttu-id="8ecf2-516">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-516">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8ecf2-517">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="8ecf2-517">Get the Order</span></span>
* <span data-ttu-id="8ecf2-518">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-518">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8ecf2-519">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="8ecf2-519">Create new Order</span></span>
* <span data-ttu-id="8ecf2-520">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-520">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="8ecf2-521">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="8ecf2-521">Remove the Order</span></span>
* <span data-ttu-id="8ecf2-522">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-522">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="8ecf2-523">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-523">Now creates Local Share</span></span>
* <span data-ttu-id="8ecf2-524">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-524">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="8ecf2-525">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-525">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="8ecf2-526">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-526">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="8ecf2-527">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-527">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="8ecf2-528">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-528">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8ecf2-529">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="8ecf2-529">Gets the information about Triggers</span></span>
* <span data-ttu-id="8ecf2-530">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-530">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8ecf2-531">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="8ecf2-531">Create new Triggers</span></span>
* <span data-ttu-id="8ecf2-532">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-532">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="8ecf2-533">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="8ecf2-533">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-534">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-535">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-535">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="8ecf2-536">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-536">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-537">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-537">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-538">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="8ecf2-538">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-539">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-539">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-540">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="8ecf2-540">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-541">Az.FrontDoor</span></span>
* <span data-ttu-id="8ecf2-542">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-542">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="8ecf2-543">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-543">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="8ecf2-544">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-544">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="8ecf2-545">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-545">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-546">Az.Network</span></span>
* <span data-ttu-id="8ecf2-547">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-547">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="8ecf2-548">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="8ecf2-548">Az.PrivateDns</span></span>
* <span data-ttu-id="8ecf2-549">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-549">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-551">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-551">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="8ecf2-552">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-552">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="8ecf2-553">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-553">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ecf2-554">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-554">Az.RedisCache</span></span>
* <span data-ttu-id="8ecf2-555">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-555">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="8ecf2-556">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-556">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="8ecf2-557">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-557">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-558">Az.Resources</span></span>
- <span data-ttu-id="8ecf2-559">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-559">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="8ecf2-560">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-560">Updated create policy definition help example</span></span>
- <span data-ttu-id="8ecf2-561">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-561">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="8ecf2-562">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-562">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="8ecf2-563">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-563">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-564">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-565">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-565">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="8ecf2-566">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="8ecf2-566">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="8ecf2-567">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-567">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="8ecf2-568">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-568">General</span></span>
* <span data-ttu-id="8ecf2-569">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-569">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-570">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-570">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-571">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-571">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8ecf2-572">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-572">Az.Advisor</span></span>
* <span data-ttu-id="8ecf2-573">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-573">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ecf2-574">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-574">Az.Batch</span></span>
* <span data-ttu-id="8ecf2-575">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-575">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="8ecf2-576">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-576">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="8ecf2-577">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-577">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="8ecf2-578">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-578">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="8ecf2-579">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-579">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="8ecf2-580">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-580">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="8ecf2-581">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-581">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="8ecf2-582">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-582">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="8ecf2-583">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-583">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="8ecf2-584">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-584">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8ecf2-585">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-585">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="8ecf2-586">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-586">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="8ecf2-587">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-587">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="8ecf2-588">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-588">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="8ecf2-589">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-589">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="8ecf2-590">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-590">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="8ecf2-591">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-591">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="8ecf2-592">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-592">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="8ecf2-593">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-593">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="8ecf2-594">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-594">This operation is no longer supported.</span></span>
* <span data-ttu-id="8ecf2-595">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-595">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8ecf2-596">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-596">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="8ecf2-597">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-597">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="8ecf2-598">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-598">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="8ecf2-599">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-599">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="8ecf2-600">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-600">New non-verified images are also now returned.</span></span> <span data-ttu-id="8ecf2-601">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-601">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="8ecf2-602">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-602">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="8ecf2-603">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-603">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="8ecf2-604">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-604">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="8ecf2-605">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-605">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="8ecf2-606">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-606">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="8ecf2-607">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-607">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="8ecf2-608">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-608">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="8ecf2-609">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-609">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="8ecf2-610">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-610">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ecf2-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-611">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-612">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-612">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="8ecf2-613">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-613">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-614">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-614">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-615">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-615">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="8ecf2-616">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-616">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="8ecf2-617">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8ecf2-617">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="8ecf2-618">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-618">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8ecf2-619">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-619">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="8ecf2-620">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="8ecf2-620">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="8ecf2-621">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-621">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="8ecf2-622">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-622">Breaking changes</span></span>
    - <span data-ttu-id="8ecf2-623">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8ecf2-623">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="8ecf2-624">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8ecf2-624">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-625">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-625">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-626">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-626">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-627">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-627">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-628">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-628">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="8ecf2-629">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-629">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="8ecf2-630">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="8ecf2-630">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="8ecf2-631">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="8ecf2-631">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="8ecf2-632">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="8ecf2-632">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="8ecf2-633">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="8ecf2-633">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-634">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-634">Az.FrontDoor</span></span>
* <span data-ttu-id="8ecf2-635">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="8ecf2-635">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-636">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-636">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-637">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-637">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="8ecf2-638">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-638">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="8ecf2-639">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-639">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="8ecf2-640">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-640">Removed five cmdlets:</span></span>
    - <span data-ttu-id="8ecf2-641">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8ecf2-641">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8ecf2-642">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8ecf2-642">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8ecf2-643">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="8ecf2-643">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="8ecf2-644">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ecf2-644">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="8ecf2-645">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ecf2-645">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="8ecf2-646">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-646">Added three cmdlets:</span></span>
    - <span data-ttu-id="8ecf2-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-647">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8ecf2-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-648">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="8ecf2-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-649">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="8ecf2-650">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-650">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="8ecf2-651">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-651">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="8ecf2-652">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-652">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="8ecf2-653">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-653">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="8ecf2-654">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-654">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="8ecf2-655">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-655">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="8ecf2-656">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-656">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="8ecf2-657">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-657">Added some scenario test cases.</span></span>
* <span data-ttu-id="8ecf2-658">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-658">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-659">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-659">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-660">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-660">Breaking changes:</span></span>
    - <span data-ttu-id="8ecf2-661">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-661">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8ecf2-662">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-662">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8ecf2-663">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-663">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8ecf2-664">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-664">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8ecf2-665">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-665">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="8ecf2-666">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-666">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="8ecf2-667">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-667">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="8ecf2-668">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-668">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="8ecf2-669">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-669">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8ecf2-670">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-670">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="8ecf2-671">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-671">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="8ecf2-672">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-672">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-673">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-673">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-674">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-674">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-675">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-675">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="8ecf2-676">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-676">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="8ecf2-677">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-677">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-678">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-678">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-679">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-679">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-680">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-680">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-681">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-681">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-682">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="8ecf2-682">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-683">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-683">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-684">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-684">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-685">Az.Network</span></span>
* <span data-ttu-id="8ecf2-686">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-686">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="8ecf2-687">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-687">Updated cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-688">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-688">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-689">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-689">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-690">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-690">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-691">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-691">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-692">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-692">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8ecf2-693">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-693">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="8ecf2-694">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-694">New cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-695">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="8ecf2-695">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="8ecf2-696">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-696">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="8ecf2-697">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-697">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="8ecf2-698">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-698">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="8ecf2-699">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-699">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="8ecf2-700">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-700">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="8ecf2-701">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-701">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="8ecf2-702">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-702">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="8ecf2-703">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-703">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-704">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-704">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="8ecf2-705">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-705">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8ecf2-706">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-706">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8ecf2-707">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-707">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="8ecf2-708">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-708">Set-AzVirtualHub</span></span>
* <span data-ttu-id="8ecf2-709">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="8ecf2-709">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="8ecf2-710">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8ecf2-711">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="8ecf2-711">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8ecf2-712">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="8ecf2-712">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="8ecf2-713">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-713">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="8ecf2-714">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-714">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="8ecf2-715">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-715">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="8ecf2-716">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-716">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-717">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-717">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="8ecf2-718">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-718">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8ecf2-719">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-719">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8ecf2-720">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-720">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8ecf2-721">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-721">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8ecf2-722">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-722">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="8ecf2-723">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-723">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="8ecf2-724">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="8ecf2-724">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="8ecf2-725">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-725">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-726">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8ecf2-726">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="8ecf2-727">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="8ecf2-727">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="8ecf2-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="8ecf2-728">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="8ecf2-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="8ecf2-729">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="8ecf2-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-730">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="8ecf2-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-731">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="8ecf2-732">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-732">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8ecf2-733">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-733">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="8ecf2-734">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-734">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="8ecf2-735">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8ecf2-735">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="8ecf2-736">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-736">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="8ecf2-737">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-737">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="8ecf2-738">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-738">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="8ecf2-739">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-739">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="8ecf2-740">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="8ecf2-740">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="8ecf2-741">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-741">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="8ecf2-742">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-742">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="8ecf2-743">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-743">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-744">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-744">New-AzIpGroup</span></span>
        - <span data-ttu-id="8ecf2-745">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-745">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="8ecf2-746">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-746">Get-AzIpGroup</span></span>
        - <span data-ttu-id="8ecf2-747">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-747">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-748">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-748">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-749">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-749">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-750">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-751">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-751">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="8ecf2-752">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-752">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="8ecf2-753">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-753">Removed deprecated aliases:</span></span>
* <span data-ttu-id="8ecf2-754">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-754">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="8ecf2-755">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-755">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="8ecf2-756">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-756">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8ecf2-757">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-757">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="8ecf2-758">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-758">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="8ecf2-759">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-759">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-760">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-761">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-761">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="8ecf2-762">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-762">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8ecf2-763">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-763">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8ecf2-764">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="8ecf2-764">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="8ecf2-765">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8ecf2-765">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="8ecf2-766">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8ecf2-766">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="8ecf2-767">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-767">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="8ecf2-768">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-768">General</span></span>
* <span data-ttu-id="8ecf2-769">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-769">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-770">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-771">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-771">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-772">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-772">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-773">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-773">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="8ecf2-774">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="8ecf2-774">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-775">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-776">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-776">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ecf2-777">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-777">Az.Batch</span></span>
* <span data-ttu-id="8ecf2-778">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-778">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-779">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-780">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-780">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="8ecf2-781">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-781">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="8ecf2-782">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-782">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="8ecf2-783">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-783">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-784">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-785">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-785">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="8ecf2-786">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-786">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="8ecf2-787">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-787">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-788">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-788">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-789">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="8ecf2-789">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="8ecf2-790">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="8ecf2-790">Az.HealthcareApis</span></span>
* <span data-ttu-id="8ecf2-791">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-791">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="8ecf2-792">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-792">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="8ecf2-793">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="8ecf2-793">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="8ecf2-794">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-794">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-795">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-795">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-796">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="8ecf2-796">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="8ecf2-797">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-797">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-798">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-798">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-799">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="8ecf2-799">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="8ecf2-800">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-800">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="8ecf2-801">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="8ecf2-801">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="8ecf2-802">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-802">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-803">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-803">Az.Network</span></span>
* <span data-ttu-id="8ecf2-804">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-804">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="8ecf2-805">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-805">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="8ecf2-806">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-806">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-807">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-807">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="8ecf2-808">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-808">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8ecf2-809">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="8ecf2-809">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="8ecf2-810">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-810">Updated cmdlets:</span></span>
        - <span data-ttu-id="8ecf2-811">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-811">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8ecf2-812">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-812">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8ecf2-813">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-813">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8ecf2-814">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="8ecf2-814">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="8ecf2-815">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="8ecf2-815">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="8ecf2-816">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-816">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="8ecf2-817">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-817">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ecf2-818">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-818">Az.RedisCache</span></span>
* <span data-ttu-id="8ecf2-819">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="8ecf2-819">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-820">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-820">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-821">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="8ecf2-821">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-822">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-823">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-823">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="8ecf2-824">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="8ecf2-824">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8ecf2-825">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8ecf2-825">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="8ecf2-826">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="8ecf2-826">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="8ecf2-827">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-827">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8ecf2-828">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8ecf2-828">Az.StorageSync</span></span>
* <span data-ttu-id="8ecf2-829">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-829">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-830">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-830">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-831">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="8ecf2-831">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="8ecf2-832">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-832">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-833">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-834">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-834">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="8ecf2-835">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-835">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="8ecf2-836">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-836">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-837">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-837">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-838">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-838">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="8ecf2-839">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="8ecf2-839">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="8ecf2-840">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-840">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-841">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-842">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-842">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="8ecf2-843">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-843">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8ecf2-844">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-844">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="8ecf2-845">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-845">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="8ecf2-846">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-846">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="8ecf2-847">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-847">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="8ecf2-848">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-848">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="8ecf2-849">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-849">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="8ecf2-850">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-850">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-851">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-851">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-852">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-852">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="8ecf2-853">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="8ecf2-853">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-854">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-854">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-855">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-855">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-856">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-857">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-857">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="8ecf2-858">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-858">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="8ecf2-859">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-859">New cmdlets are:</span></span>
    - <span data-ttu-id="8ecf2-860">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-860">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8ecf2-861">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-861">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8ecf2-862">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-862">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="8ecf2-863">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-863">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-864">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-864">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-865">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-865">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="8ecf2-866">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-866">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="8ecf2-867">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-867">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="8ecf2-868">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-868">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="8ecf2-869">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-869">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="8ecf2-870">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-870">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="8ecf2-871">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-871">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="8ecf2-872">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-872">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="8ecf2-873">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-873">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8ecf2-874">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-874">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="8ecf2-875">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-875">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="8ecf2-876">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-876">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="8ecf2-877">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-877">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="8ecf2-878">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="8ecf2-878">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="8ecf2-879">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="8ecf2-879">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="8ecf2-880">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-880">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="8ecf2-881">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-881">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="8ecf2-882">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-882">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="8ecf2-883">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-883">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="8ecf2-884">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-884">Overall improved help files</span></span>
* <span data-ttu-id="8ecf2-885">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-885">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-886">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-886">Az.Network</span></span>
* <span data-ttu-id="8ecf2-887">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-887">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="8ecf2-888">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-888">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="8ecf2-889">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="8ecf2-889">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="8ecf2-890">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-890">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="8ecf2-891">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="8ecf2-891">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="8ecf2-892">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8ecf2-892">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="8ecf2-893">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-893">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="8ecf2-894">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8ecf2-894">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="8ecf2-895">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-895">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="8ecf2-896">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-896">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="8ecf2-897">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-897">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="8ecf2-898">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-898">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="8ecf2-899">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-899">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-900">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="8ecf2-900">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="8ecf2-901">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-901">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="8ecf2-902">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-902">Updated cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-903">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-903">New-VpnSite</span></span>
        - <span data-ttu-id="8ecf2-904">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-904">Update-VpnSite</span></span>
        - <span data-ttu-id="8ecf2-905">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-905">New-VpnConnection</span></span>
        - <span data-ttu-id="8ecf2-906">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-906">Update-VpnConnection</span></span>
* <span data-ttu-id="8ecf2-907">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-907">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-908">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-908">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-909">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-909">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="8ecf2-910">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-910">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-911">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-912">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-912">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-914">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-914">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="8ecf2-915">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-915">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="8ecf2-916">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8ecf2-916">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8ecf2-917">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-917">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8ecf2-918">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8ecf2-918">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8ecf2-919">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-919">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="8ecf2-920">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8ecf2-920">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8ecf2-921">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8ecf2-921">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8ecf2-922">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-922">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8ecf2-923">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8ecf2-923">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8ecf2-924">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-924">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="8ecf2-925">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8ecf2-925">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="8ecf2-926">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-926">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="8ecf2-927">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8ecf2-927">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="8ecf2-928">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="8ecf2-928">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="8ecf2-929">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-929">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ecf2-930">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ecf2-930">Az.SignalR</span></span>
* <span data-ttu-id="8ecf2-931">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-931">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-932">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-933">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-933">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="8ecf2-934">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-934">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="8ecf2-935">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-935">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8ecf2-936">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-936">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="8ecf2-937">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-937">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-938">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-938">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-939">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-939">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="8ecf2-940">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-940">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="8ecf2-941">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-941">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="8ecf2-942">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-942">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="8ecf2-943">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-943">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="8ecf2-944">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-944">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="8ecf2-945">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-945">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="8ecf2-946">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-946">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8ecf2-947">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-947">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8ecf2-948">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-948">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="8ecf2-949">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-949">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-950">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-950">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-951">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="8ecf2-951">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="8ecf2-952">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="8ecf2-952">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="8ecf2-953">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-953">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="8ecf2-954">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-954">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="8ecf2-955">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-955">General</span></span>
* <span data-ttu-id="8ecf2-956">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="8ecf2-956">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-957">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-958">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-958">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="8ecf2-959">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8ecf2-959">Az.Aks</span></span>
* <span data-ttu-id="8ecf2-960">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-960">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="8ecf2-961">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="8ecf2-961">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-962">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-963">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="8ecf2-963">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="8ecf2-964">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-964">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="8ecf2-965">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-965">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="8ecf2-966">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="8ecf2-966">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="8ecf2-967">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-967">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ecf2-968">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-968">Az.Batch</span></span>
* <span data-ttu-id="8ecf2-969">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="8ecf2-969">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ecf2-970">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-970">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-971">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="8ecf2-971">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-972">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-972">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-973">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-973">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="8ecf2-974">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-974">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="8ecf2-975">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-975">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="8ecf2-976">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-976">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="8ecf2-977">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8ecf2-977">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="8ecf2-978">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-978">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="8ecf2-979">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-979">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="8ecf2-980">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-980">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-981">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-982">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="8ecf2-982">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="8ecf2-983">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-983">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="8ecf2-984">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="8ecf2-984">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="8ecf2-985">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="8ecf2-985">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-986">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-987">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-987">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-988">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-988">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-989">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-989">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="8ecf2-990">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="8ecf2-990">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="8ecf2-991">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="8ecf2-991">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="8ecf2-992">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-992">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="8ecf2-993">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8ecf2-993">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8ecf2-994">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-994">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-995">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-995">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-996">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-996">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-997">Az.Network</span></span>
* <span data-ttu-id="8ecf2-998">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-998">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="8ecf2-999">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-999">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="8ecf2-1000">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1000">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="8ecf2-1001">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1001">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="8ecf2-1002">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1002">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="8ecf2-1003">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1003">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="8ecf2-1004">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1004">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ecf2-1006">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1006">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="8ecf2-1007">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1007">Added example</span></span>
    - <span data-ttu-id="8ecf2-1008">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1008">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="8ecf2-1009">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1009">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="8ecf2-1010">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1010">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1011">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1011">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1012">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1012">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1013">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1013">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1014">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1014">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="8ecf2-1015">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1015">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="8ecf2-1016">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1016">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="8ecf2-1017">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1017">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ecf2-1018">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1018">Az.ServiceBus</span></span>
* <span data-ttu-id="8ecf2-1019">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1019">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="8ecf2-1020">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1020">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="8ecf2-1021">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1021">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-1022">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1022">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-1023">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1023">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="8ecf2-1024">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1024">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="8ecf2-1025">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1025">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="8ecf2-1026">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1026">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="8ecf2-1027">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1027">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="8ecf2-1028">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1028">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1029">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1030">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1030">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1031">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1032">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1032">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="8ecf2-1033">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1033">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="8ecf2-1034">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1034">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="8ecf2-1035">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1035">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="8ecf2-1036">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1036">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="8ecf2-1037">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1037">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1038">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1039">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1039">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="8ecf2-1040">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1040">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1041">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1042">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1042">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="8ecf2-1043">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1043">Az.ApplicationInsights</span></span>
* <span data-ttu-id="8ecf2-1044">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1044">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1045">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1046">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1046">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-1047">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1047">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-1048">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1048">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1049">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1049">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1050">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1050">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8ecf2-1051">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1051">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8ecf2-1052">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1052">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="8ecf2-1053">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1053">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-1054">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1054">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-1055">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1055">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="8ecf2-1056">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1056">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-1057">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1057">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-1058">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1058">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8ecf2-1059">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1059">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-1060">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1060">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-1061">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1061">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ecf2-1062">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1062">Az.LogicApp</span></span>
* <span data-ttu-id="8ecf2-1063">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1063">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="8ecf2-1064">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1064">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="8ecf2-1065">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1065">Az.ManagedServices</span></span>
* <span data-ttu-id="8ecf2-1066">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1066">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1067">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1067">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1068">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1068">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="8ecf2-1069">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1069">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1070">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1070">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ecf2-1071">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1071">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ecf2-1072">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1072">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-1073">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1073">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-1074">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1074">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-1075">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1075">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="8ecf2-1076">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1076">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="8ecf2-1077">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1077">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="8ecf2-1078">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1078">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="8ecf2-1079">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1079">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="8ecf2-1080">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1080">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="8ecf2-1081">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1081">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="8ecf2-1082">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1082">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="8ecf2-1083">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1083">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="8ecf2-1084">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1084">Updated cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1085">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1085">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8ecf2-1086">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1086">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="8ecf2-1087">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1087">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="8ecf2-1088">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1088">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8ecf2-1089">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1089">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="8ecf2-1090">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1090">Updated cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-1091">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1091">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8ecf2-1092">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1092">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="8ecf2-1093">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1093">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="8ecf2-1094">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1094">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="8ecf2-1095">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1095">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="8ecf2-1096">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1096">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1097">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1097">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ecf2-1098">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1098">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="8ecf2-1099">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1099">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1100">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1100">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1101">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1101">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8ecf2-1102">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1102">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="8ecf2-1103">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1103">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="8ecf2-1104">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1104">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="8ecf2-1105">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1105">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="8ecf2-1106">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1106">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8ecf2-1107">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1107">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="8ecf2-1108">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1108">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="8ecf2-1109">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1109">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="8ecf2-1110">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1110">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1111">Az.Resources</span></span>
- <span data-ttu-id="8ecf2-1112">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1112">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="8ecf2-1113">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1113">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ecf2-1114">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1114">Az.ServiceBus</span></span>
* <span data-ttu-id="8ecf2-1115">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1115">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="8ecf2-1116">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1116">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1117">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1118">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1118">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="8ecf2-1119">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1119">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="8ecf2-1120">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1120">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1121">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1122">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1122">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8ecf2-1123">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1123">Az.StorageSync</span></span>
* <span data-ttu-id="8ecf2-1124">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1124">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="8ecf2-1125">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1125">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1126">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1127">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1127">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="8ecf2-1128">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1128">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="8ecf2-1129">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1129">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="8ecf2-1130">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1130">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1131">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1131">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1132">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1132">Add support for profile cmdlets</span></span>
* <span data-ttu-id="8ecf2-1133">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1133">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="8ecf2-1134">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1134">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="8ecf2-1135">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1135">Az.Advisor</span></span>
* <span data-ttu-id="8ecf2-1136">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1136">GA release of Az.Advisor</span></span>
* <span data-ttu-id="8ecf2-1137">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1137">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-1138">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1138">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-1139">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1139">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="8ecf2-1140">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1140">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="8ecf2-1141">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1141">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="8ecf2-1142">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1142">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="8ecf2-1143">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1143">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="8ecf2-1144">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1144">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="8ecf2-1145">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1145">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1146">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1146">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1147">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1147">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1148">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1148">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1149">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1149">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1150">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-1151">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1151">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ecf2-1152">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1152">Az.EventGrid</span></span>
* <span data-ttu-id="8ecf2-1153">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1153">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1154">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-1155">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1155">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1156">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1157">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1157">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="8ecf2-1158">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1158">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ecf2-1159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1159">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ecf2-1160">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1160">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="8ecf2-1161">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1161">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1162">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1162">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ecf2-1163">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1163">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1165">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1165">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1166">Az.Resources</span></span>
    - <span data-ttu-id="8ecf2-1167">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1167">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="8ecf2-1168">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1168">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="8ecf2-1169">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1169">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="8ecf2-1170">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1170">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ecf2-1171">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1171">Az.ServiceBus</span></span>
* <span data-ttu-id="8ecf2-1172">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1172">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1173">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1174">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1174">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="8ecf2-1175">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1175">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="8ecf2-1176">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1176">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8ecf2-1177">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1177">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8ecf2-1178">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1178">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="8ecf2-1179">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1179">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8ecf2-1180">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1180">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="8ecf2-1181">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1181">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="8ecf2-1182">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1182">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1183">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1183">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1184">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1184">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="8ecf2-1185">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1185">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="8ecf2-1186">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1186">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="8ecf2-1187">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1187">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="8ecf2-1188">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1188">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="8ecf2-1189">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1189">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="8ecf2-1190">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1190">Set-AzStorageAccount</span></span>
* <span data-ttu-id="8ecf2-1191">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1191">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="8ecf2-1192">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1192">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="8ecf2-1193">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1193">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="8ecf2-1194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1194">Az.StorageSync</span></span>
* <span data-ttu-id="8ecf2-1195">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1195">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="8ecf2-1196">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1196">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1197">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1197">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1198">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1198">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="8ecf2-1199">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1199">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="8ecf2-1200">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1200">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="8ecf2-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1201">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="8ecf2-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1202">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1203">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1203">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1204">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1204">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="8ecf2-1205">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1205">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="8ecf2-1206">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1206">Az.Dns</span></span>
* <span data-ttu-id="8ecf2-1207">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1207">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ecf2-1208">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1208">Az.EventGrid</span></span>
* <span data-ttu-id="8ecf2-1209">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1209">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="8ecf2-1210">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1210">New cmdlets:</span></span>
    - <span data-ttu-id="8ecf2-1211">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1211">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8ecf2-1212">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1212">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8ecf2-1213">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1213">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8ecf2-1214">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1214">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="8ecf2-1215">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1215">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="8ecf2-1216">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1216">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8ecf2-1217">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1217">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8ecf2-1218">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1218">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="8ecf2-1219">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1219">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="8ecf2-1220">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1220">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="8ecf2-1221">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1221">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8ecf2-1222">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1222">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="8ecf2-1223">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1223">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="8ecf2-1224">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1224">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="8ecf2-1225">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1225">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="8ecf2-1226">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1226">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="8ecf2-1227">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1227">Updated cmdlets:</span></span>
    - <span data-ttu-id="8ecf2-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1228">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="8ecf2-1229">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1229">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8ecf2-1230">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1230">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="8ecf2-1231">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1231">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="8ecf2-1232">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1232">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="8ecf2-1233">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1233">Event subscription expiration date,</span></span>
            - <span data-ttu-id="8ecf2-1234">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1234">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="8ecf2-1235">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1235">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="8ecf2-1236">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1236">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="8ecf2-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1237">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="8ecf2-1238">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1238">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="8ecf2-1239">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1239">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="8ecf2-1240">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1240">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="8ecf2-1241">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1241">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-1242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1242">Az.FrontDoor</span></span>
* <span data-ttu-id="8ecf2-1243">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1243">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="8ecf2-1244">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1244">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="8ecf2-1245">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1245">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="8ecf2-1246">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1246">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1247">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1248">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1248">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="8ecf2-1249">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1249">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1250">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="8ecf2-1251">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1251">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="8ecf2-1252">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1252">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1253">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1253">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="8ecf2-1254">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1254">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="8ecf2-1255">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1255">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1256">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1256">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ecf2-1257">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1257">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ecf2-1258">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1258">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="8ecf2-1259">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1259">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="8ecf2-1260">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1260">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="8ecf2-1261">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1261">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="8ecf2-1262">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1262">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1263">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1263">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ecf2-1264">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1264">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ecf2-1265">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1265">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="8ecf2-1266">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1266">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="8ecf2-1267">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1267">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="8ecf2-1268">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1268">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="8ecf2-1269">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1269">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="8ecf2-1270">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1270">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="8ecf2-1271">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1271">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="8ecf2-1272">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1272">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="8ecf2-1273">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1273">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="8ecf2-1274">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1274">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="8ecf2-1275">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1275">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="8ecf2-1276">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1276">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="8ecf2-1277">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1277">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="8ecf2-1278">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1278">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="8ecf2-1279">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1279">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="8ecf2-1280">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1280">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="8ecf2-1281">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1281">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-1282">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1282">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="8ecf2-1283">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1283">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="8ecf2-1284">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1284">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="8ecf2-1285">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1285">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="8ecf2-1286">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1286">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="8ecf2-1287">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1287">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8ecf2-1288">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1288">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="8ecf2-1289">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1289">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1290">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1290">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ecf2-1291">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1291">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1292">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1293">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1293">Support for additional Template Export options</span></span>
    - <span data-ttu-id="8ecf2-1294">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1294">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8ecf2-1295">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1295">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="8ecf2-1296">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1296">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-1297">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1297">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-1298">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1298">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1299">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1299">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1300">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1300">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="8ecf2-1301">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1301">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="8ecf2-1302">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1302">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="8ecf2-1303">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1303">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8ecf2-1304">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1304">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8ecf2-1305">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1305">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="8ecf2-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1306">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="8ecf2-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1307">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1308">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1309">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1309">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="8ecf2-1310">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1310">New-AzStorageAccount</span></span>
* <span data-ttu-id="8ecf2-1311">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1311">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="8ecf2-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1312">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1313">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1314">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1314">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="8ecf2-1315">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1315">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="8ecf2-1316">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1316">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="8ecf2-1317">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1317">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-1318">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1318">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1319">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1320">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1320">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="8ecf2-1321">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1321">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-1322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1322">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-1323">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1323">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="8ecf2-1324">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1324">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1325">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1326">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1326">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="8ecf2-1327">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1327">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ecf2-1328">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1328">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ecf2-1329">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1329">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1330">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1331">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1331">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ecf2-1332">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1332">Az.ServiceBus</span></span>
* <span data-ttu-id="8ecf2-1333">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1333">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-1334">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1334">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-1335">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1335">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="8ecf2-1336">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1336">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1337">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1338">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1338">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="8ecf2-1339">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1339">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="8ecf2-1340">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1340">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="8ecf2-1341">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1341">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1342">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1342">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1343">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1343">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="8ecf2-1344">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1344">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-1345">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1345">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-1346">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1346">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="8ecf2-1347">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1347">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="8ecf2-1348">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1348">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="8ecf2-1349">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1349">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="8ecf2-1350">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1350">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="8ecf2-1351">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1351">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="8ecf2-1352">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1352">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="8ecf2-1353">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1353">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="8ecf2-1354">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1354">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="8ecf2-1355">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1355">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="8ecf2-1356">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1356">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="8ecf2-1357">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1357">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="8ecf2-1358">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1358">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="8ecf2-1359">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1359">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="8ecf2-1360">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1360">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="8ecf2-1361">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1361">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="8ecf2-1362">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1362">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="8ecf2-1363">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1363">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="8ecf2-1364">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1364">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="8ecf2-1365">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1365">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="8ecf2-1366">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1366">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="8ecf2-1367">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1367">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="8ecf2-1368">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1368">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="8ecf2-1369">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1369">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="8ecf2-1370">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1370">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="8ecf2-1371">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1371">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="8ecf2-1372">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1372">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="8ecf2-1373">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1373">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="8ecf2-1374">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1374">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="8ecf2-1375">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1375">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="8ecf2-1376">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1376">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="8ecf2-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1377">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="8ecf2-1378">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1378">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="8ecf2-1379">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1379">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8ecf2-1380">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1380">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="8ecf2-1381">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1381">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="8ecf2-1382">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1382">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="8ecf2-1383">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1383">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="8ecf2-1384">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1384">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="8ecf2-1385">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1385">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8ecf2-1386">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1386">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8ecf2-1387">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1387">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8ecf2-1388">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1388">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="8ecf2-1389">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1389">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8ecf2-1390">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1390">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="8ecf2-1391">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1391">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="8ecf2-1392">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1392">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="8ecf2-1393">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1393">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="8ecf2-1394">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1394">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="8ecf2-1395">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1395">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="8ecf2-1396">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1396">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="8ecf2-1397">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1397">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="8ecf2-1398">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1398">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="8ecf2-1399">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1399">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="8ecf2-1400">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1400">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="8ecf2-1401">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1401">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="8ecf2-1402">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1402">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8ecf2-1403">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1403">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8ecf2-1404">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1404">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8ecf2-1405">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1405">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8ecf2-1406">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1406">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="8ecf2-1407">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1407">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="8ecf2-1408">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1408">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="8ecf2-1409">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1409">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="8ecf2-1410">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1410">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="8ecf2-1411">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1411">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="8ecf2-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1412">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="8ecf2-1413">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1413">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="8ecf2-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1414">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="8ecf2-1415">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1415">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="8ecf2-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1416">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="8ecf2-1417">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1417">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="8ecf2-1418">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1418">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="8ecf2-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1419">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="8ecf2-1420">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1420">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="8ecf2-1421">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1421">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="8ecf2-1422">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1422">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1423">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1423">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1424">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1424">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="8ecf2-1425">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1425">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="8ecf2-1426">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1426">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="8ecf2-1427">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1427">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="8ecf2-1428">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1428">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="8ecf2-1429">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1429">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="8ecf2-1430">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1430">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1431">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1432">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1432">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="8ecf2-1433">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1433">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-1434">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1434">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-1435">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1435">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-1436">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1436">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-1437">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1437">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1438">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1438">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1439">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1439">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="8ecf2-1440">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1440">Updated cmdlet:</span></span>
        - <span data-ttu-id="8ecf2-1441">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1441">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="8ecf2-1442">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1442">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1443">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1443">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1444">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1444">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1445">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1445">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1446">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1446">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="8ecf2-1447">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1447">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1448">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1448">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1449">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1449">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-1450">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1450">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-1451">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1451">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="8ecf2-1452">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1452">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1453">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1454">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1454">Proximity placement group feature.</span></span>
    - <span data-ttu-id="8ecf2-1455">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1455">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="8ecf2-1456">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1456">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="8ecf2-1457">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1457">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="8ecf2-1458">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1458">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="8ecf2-1459">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1459">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="8ecf2-1460">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1460">Breaking changes</span></span>
    - <span data-ttu-id="8ecf2-1461">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1461">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="8ecf2-1462">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1462">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="8ecf2-1463">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1463">Az.DeploymentManager</span></span>
* <span data-ttu-id="8ecf2-1464">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1464">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="8ecf2-1465">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1465">Az.Dns</span></span>
* <span data-ttu-id="8ecf2-1466">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1466">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="8ecf2-1467">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1467">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="8ecf2-1468">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1468">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-1469">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1469">Az.FrontDoor</span></span>
* <span data-ttu-id="8ecf2-1470">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1470">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="8ecf2-1471">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1471">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1472">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-1473">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1473">Removed two cmdlets:</span></span>
    - <span data-ttu-id="8ecf2-1474">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1474">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="8ecf2-1475">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1475">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8ecf2-1476">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1476">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="8ecf2-1477">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1477">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="8ecf2-1478">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1478">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="8ecf2-1479">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1479">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-1480">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1480">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-1481">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1481">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="8ecf2-1482">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1482">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="8ecf2-1483">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1483">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="8ecf2-1484">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1484">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="8ecf2-1485">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1485">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="8ecf2-1486">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1486">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="8ecf2-1487">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1487">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="8ecf2-1488">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1488">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ecf2-1489">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1489">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ecf2-1490">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1490">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ecf2-1491">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1491">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ecf2-1492">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1492">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="8ecf2-1493">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1493">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="8ecf2-1494">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1494">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1495">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1496">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1496">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="8ecf2-1497">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1497">New cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1498">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1498">New-AzNatGateway</span></span>
        - <span data-ttu-id="8ecf2-1499">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1499">Get-AzNatGateway</span></span>
        - <span data-ttu-id="8ecf2-1500">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1500">Set-AzNatGateway</span></span>
        - <span data-ttu-id="8ecf2-1501">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1501">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="8ecf2-1502">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1502">Updated cmdlets</span></span>
        - <span data-ttu-id="8ecf2-1503">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1503">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="8ecf2-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1504">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="8ecf2-1505">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1505">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="8ecf2-1506">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1506">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="8ecf2-1507">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1507">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ecf2-1508">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1508">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ecf2-1509">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1509">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="8ecf2-1510">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1510">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="8ecf2-1511">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1511">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1512">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1513">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1513">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="8ecf2-1514">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1514">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="8ecf2-1515">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1515">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="8ecf2-1516">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1516">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="8ecf2-1517">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1517">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="8ecf2-1518">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1518">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="8ecf2-1519">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1519">Az.Relay</span></span>
* <span data-ttu-id="8ecf2-1520">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1520">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ecf2-1521">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1521">Az.ServiceBus</span></span>
* <span data-ttu-id="8ecf2-1522">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1522">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1523">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1524">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1524">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="8ecf2-1525">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1525">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="8ecf2-1526">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1526">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="8ecf2-1527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1527">New-AzStorageAccount</span></span>
* <span data-ttu-id="8ecf2-1528">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1528">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="8ecf2-1529">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1529">New-AzStorageAccount</span></span>
    - <span data-ttu-id="8ecf2-1530">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1530">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="8ecf2-1531">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1531">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1532">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1533">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1533">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="8ecf2-1534">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1534">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="8ecf2-1535">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1535">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ecf2-1536">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1536">Highlights since the last major release</span></span>
* <span data-ttu-id="8ecf2-1537">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1537">General availability of `Az` module</span></span>
* <span data-ttu-id="8ecf2-1538">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1538">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ecf2-1539">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1539">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ecf2-1540">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1540">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ecf2-1541">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1541">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ecf2-1542">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1542">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1543">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1543">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1544">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1544">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1545">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1545">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="8ecf2-1546">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1546">Az.Batch</span></span>
* <span data-ttu-id="8ecf2-1547">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ecf2-1548">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1548">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-1549">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1549">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-1550">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1550">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-1551">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1551">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1552">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1552">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1553">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1553">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="8ecf2-1554">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1554">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ecf2-1555">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1555">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-1556">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1556">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-1557">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1557">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-1559">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1559">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ecf2-1560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1560">Az.EventGrid</span></span>
* <span data-ttu-id="8ecf2-1561">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1561">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-1562">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1562">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-1563">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1563">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="8ecf2-1564">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1564">Az.HDInsight</span></span>
* <span data-ttu-id="8ecf2-1565">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-1566">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1566">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-1567">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-1568">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1568">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-1569">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ecf2-1570">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1570">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="8ecf2-1571">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1571">Az.MachineLearning</span></span>
* <span data-ttu-id="8ecf2-1572">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1572">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="8ecf2-1573">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1573">Az.Media</span></span>
* <span data-ttu-id="8ecf2-1574">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-1575">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1575">Az.Monitor</span></span>
  * <span data-ttu-id="8ecf2-1576">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1576">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="8ecf2-1577">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1577">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="8ecf2-1578">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1578">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="8ecf2-1579">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1579">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8ecf2-1580">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1580">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="8ecf2-1581">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1581">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="8ecf2-1582">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1582">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1583">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1584">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1584">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ecf2-1585">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1585">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="8ecf2-1586">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1586">Az.NotificationHubs</span></span>
* <span data-ttu-id="8ecf2-1587">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1588">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1588">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ecf2-1589">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="8ecf2-1590">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1590">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="8ecf2-1591">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1591">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1593">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ecf2-1594">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1594">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="8ecf2-1595">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1595">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="8ecf2-1596">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1596">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ecf2-1597">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1597">Az.RedisCache</span></span>
* <span data-ttu-id="8ecf2-1598">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1599">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1599">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1600">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1600">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1601">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1601">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1602">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1602">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="8ecf2-1603">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ecf2-1604">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1604">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="8ecf2-1605">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1605">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="8ecf2-1606">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1606">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="8ecf2-1607">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1607">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="8ecf2-1608">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1608">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1609">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1610">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1610">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="8ecf2-1611">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="8ecf2-1612">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1612">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="8ecf2-1613">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1613">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="8ecf2-1614">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1614">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ecf2-1615">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1615">Highlights since the last major release</span></span>
* <span data-ttu-id="8ecf2-1616">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1616">General availability of `Az` module</span></span>
* <span data-ttu-id="8ecf2-1617">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1617">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ecf2-1618">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1618">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ecf2-1619">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1619">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ecf2-1620">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1620">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ecf2-1621">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1621">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1622">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1622">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1623">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1624">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1624">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ecf2-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1625">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ecf2-1626">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1626">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="8ecf2-1627">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1627">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1628">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1628">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1629">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1629">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="8ecf2-1630">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1630">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="8ecf2-1631">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1631">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1632">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1633">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1633">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="8ecf2-1634">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1634">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="8ecf2-1635">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1635">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ecf2-1636">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1636">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-1637">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1637">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-1638">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1638">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="8ecf2-1639">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1639">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1640">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1640">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1641">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1641">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="8ecf2-1642">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1642">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="8ecf2-1643">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1643">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="8ecf2-1644">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1644">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="8ecf2-1645">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1645">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="8ecf2-1646">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1646">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1647">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1647">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1648">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1648">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1649">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1649">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1650">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1650">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="8ecf2-1651">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1651">New-AzStorageContext</span></span>
* <span data-ttu-id="8ecf2-1652">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1652">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="8ecf2-1653">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1653">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8ecf2-1654">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1654">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="8ecf2-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1655">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="8ecf2-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1656">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="8ecf2-1657">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1657">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="8ecf2-1658">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1658">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8ecf2-1659">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1659">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="8ecf2-1660">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1660">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="8ecf2-1661">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1661">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="8ecf2-1662">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1662">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="8ecf2-1663">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1663">Highlights since the last major release</span></span>
* <span data-ttu-id="8ecf2-1664">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1664">General availability of `Az` module</span></span>
* <span data-ttu-id="8ecf2-1665">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1665">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="8ecf2-1666">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1666">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="8ecf2-1667">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1667">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="8ecf2-1668">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1668">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ecf2-1669">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1669">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1670">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1670">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1671">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1671">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1672">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1672">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="8ecf2-1673">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1673">Dynamic grouping</span></span>
    * <span data-ttu-id="8ecf2-1674">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1674">Pre-Post script</span></span>
    * <span data-ttu-id="8ecf2-1675">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1675">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1676">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1677">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1677">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="8ecf2-1678">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1678">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-1679">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1679">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-1680">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1680">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1681">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1682">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1682">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="8ecf2-1683">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1683">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1684">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1684">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1685">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1685">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="8ecf2-1686">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1686">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1687">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1688">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1688">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="8ecf2-1689">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1689">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1690">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1690">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1691">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1691">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1692">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1693">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1693">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="8ecf2-1694">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1694">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ecf2-1695">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1695">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ecf2-1696">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1696">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="8ecf2-1697">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1697">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="8ecf2-1698">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1698">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="8ecf2-1699">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1699">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1700">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1700">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1701">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1701">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="8ecf2-1702">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1702">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1703">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1703">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1704">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1704">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="8ecf2-1705">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1705">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1706">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1707">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1707">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="8ecf2-1708">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1708">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="8ecf2-1709">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1709">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ecf2-1710">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1710">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-1711">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1711">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1712">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1713">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1713">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-1714">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1714">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-1715">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1715">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ecf2-1716">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1716">Az.LogicApp</span></span>
* <span data-ttu-id="8ecf2-1717">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1717">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1718">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1719">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1719">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1720">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1720">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1721">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1721">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="8ecf2-1722">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1722">SDK Update</span></span>
* <span data-ttu-id="8ecf2-1723">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1723">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="8ecf2-1724">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1724">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1725">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1726">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1726">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="8ecf2-1727">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1727">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="8ecf2-1728">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1728">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="8ecf2-1729">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1729">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="8ecf2-1730">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1730">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="8ecf2-1731">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1731">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1732">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1732">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1733">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1733">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="8ecf2-1734">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1734">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1735">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1736">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1736">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="8ecf2-1737">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1737">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="8ecf2-1738">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1738">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ecf2-1739">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1739">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1740">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1740">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1741">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1741">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="8ecf2-1742">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1742">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="8ecf2-1743">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1743">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-1744">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1744">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-1745">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1745">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1746">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1747">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1747">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="8ecf2-1748">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1748">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="8ecf2-1749">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1749">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="8ecf2-1750">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1750">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-1751">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1751">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-1752">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1752">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="8ecf2-1753">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1753">Az.EventHub</span></span>
* <span data-ttu-id="8ecf2-1754">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1754">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-1755">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1755">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-1756">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1756">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ecf2-1757">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1757">Az.LogicApp</span></span>
* <span data-ttu-id="8ecf2-1758">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1758">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="8ecf2-1759">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1759">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="8ecf2-1760">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1760">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="8ecf2-1761">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1761">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ecf2-1762">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1762">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ecf2-1763">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1763">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="8ecf2-1764">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1764">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="8ecf2-1765">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1765">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="8ecf2-1766">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1766">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ecf2-1767">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1767">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ecf2-1768">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1768">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="8ecf2-1769">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1769">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="8ecf2-1770">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1770">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="8ecf2-1771">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1771">Az.Monitor</span></span>
* <span data-ttu-id="8ecf2-1772">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1772">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1773">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1774">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1774">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1775">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1775">Az.OperationalInsights</span></span>
* <span data-ttu-id="8ecf2-1776">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1776">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="8ecf2-1777">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1777">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="8ecf2-1778">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1778">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1779">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1780">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1780">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8ecf2-1781">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="8ecf2-1782">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1782">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="8ecf2-1783">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1783">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1784">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1785">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1785">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="8ecf2-1786">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1786">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1787">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1787">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1788">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1788">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="8ecf2-1789">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1789">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1790">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1791">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1791">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ecf2-1792">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1792">Az.AnalysisServices</span></span>
<span data-ttu-id="8ecf2-1793">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1793">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1794">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1795">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1795">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="8ecf2-1796">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1796">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="8ecf2-1797">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1797">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1798">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1798">Az.RecoveryServices</span></span>
<span data-ttu-id="8ecf2-1799">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1799">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1800">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1800">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1801">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1801">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="8ecf2-1802">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1802">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="8ecf2-1803">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1803">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="8ecf2-1804">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1804">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1805">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1806">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1806">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="8ecf2-1807">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1807">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="8ecf2-1808">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1808">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="8ecf2-1809">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1809">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1810">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1811">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1811">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="8ecf2-1812">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1812">Az.AnalysisServices</span></span>
* <span data-ttu-id="8ecf2-1813">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1813">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1814">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1814">Az.RecoveryServices</span></span>
* <span data-ttu-id="8ecf2-1815">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1815">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="8ecf2-1816">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1816">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1817">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1817">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1818">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1818">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="8ecf2-1819">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1819">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ecf2-1820">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1820">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="8ecf2-1821">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1821">Az.Aks</span></span>
* <span data-ttu-id="8ecf2-1822">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1822">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="8ecf2-1823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1823">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-1824">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1824">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="8ecf2-1825">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1825">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="8ecf2-1826">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1826">Az.Cdn</span></span>
* <span data-ttu-id="8ecf2-1827">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1827">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1828">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1828">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1829">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1829">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="8ecf2-1830">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1830">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="8ecf2-1831">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1831">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="8ecf2-1832">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1832">Az.ContainerRegistry</span></span>
* <span data-ttu-id="8ecf2-1833">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1833">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="8ecf2-1834">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1834">Az.DataFactory</span></span>
* <span data-ttu-id="8ecf2-1835">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1835">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-1836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1836">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-1837">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1837">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="8ecf2-1838">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1838">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="8ecf2-1839">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1839">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-1840">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1840">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-1841">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1841">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-1842">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1842">Az.KeyVault</span></span>
* <span data-ttu-id="8ecf2-1843">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1843">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1844">Az.Network</span></span>
* <span data-ttu-id="8ecf2-1845">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1845">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1846">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1847">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1847">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="8ecf2-1848">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1848">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="8ecf2-1849">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1849">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="8ecf2-1850">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1850">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="8ecf2-1851">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1851">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="8ecf2-1852">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1852">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="8ecf2-1853">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1853">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-1854">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1854">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-1855">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1855">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="8ecf2-1856">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1856">Fix some error messages.</span></span>
* <span data-ttu-id="8ecf2-1857">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1857">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="8ecf2-1858">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1858">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ecf2-1859">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1859">Az.SignalR</span></span>
* <span data-ttu-id="8ecf2-1860">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1860">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1861">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1862">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1862">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ecf2-1863">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1863">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="8ecf2-1864">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1864">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="8ecf2-1865">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1865">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1866">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1866">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1867">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1867">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ecf2-1868">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1868">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="8ecf2-1869">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1869">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="8ecf2-1870">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1870">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="8ecf2-1871">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1871">Az.TrafficManager</span></span>
* <span data-ttu-id="8ecf2-1872">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1872">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1873">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1873">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1874">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1874">Update incorrect online help URLs</span></span>
* <span data-ttu-id="8ecf2-1875">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1875">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="8ecf2-1876">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1876">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="8ecf2-1877">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1877">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1878">Az.Accounts</span></span>
* <span data-ttu-id="8ecf2-1879">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1879">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1880">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-1881">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1881">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="8ecf2-1882">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1882">Updated the description of ID in help files</span></span>
* <span data-ttu-id="8ecf2-1883">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-1884">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1884">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-1885">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1885">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="8ecf2-1886">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1886">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="8ecf2-1887">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1887">Az.EventGrid</span></span>
* <span data-ttu-id="8ecf2-1888">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1888">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="8ecf2-1889">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1889">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="8ecf2-1890">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1890">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8ecf2-1891">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1891">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8ecf2-1892">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1892">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8ecf2-1893">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1893">Dead letter endpoint.</span></span>
    - <span data-ttu-id="8ecf2-1894">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1894">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="8ecf2-1895">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1895">Event Time-To-Live,</span></span>
        - <span data-ttu-id="8ecf2-1896">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1896">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="8ecf2-1897">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1897">Dead letter endpoint.</span></span>
* <span data-ttu-id="8ecf2-1898">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1898">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="8ecf2-1899">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1899">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="8ecf2-1900">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1900">Az.IotHub</span></span>
* <span data-ttu-id="8ecf2-1901">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1901">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="8ecf2-1902">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1902">Az.LogicApp</span></span>
* <span data-ttu-id="8ecf2-1903">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1903">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-1904">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1904">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-1905">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1905">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="8ecf2-1906">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1906">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="8ecf2-1907">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1907">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8ecf2-1908">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1908">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="8ecf2-1909">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1909">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="8ecf2-1910">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1910">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="8ecf2-1911">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1911">Az.SignalR</span></span>
* <span data-ttu-id="8ecf2-1912">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1912">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1913">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-1914">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1914">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="8ecf2-1915">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1915">Az.Storage</span></span>
* <span data-ttu-id="8ecf2-1916">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1916">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="8ecf2-1917">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1917">New-AzStorageContext</span></span>
* <span data-ttu-id="8ecf2-1918">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1918">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="8ecf2-1919">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1919">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1920">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-1921">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1921">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="8ecf2-1922">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1922">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="8ecf2-1923">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1923">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="8ecf2-1924">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1924">General</span></span>

- <span data-ttu-id="8ecf2-1925">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1925">General Availability of Az Module</span></span>
- <span data-ttu-id="8ecf2-1926">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1926">Online help for each module</span></span>
- <span data-ttu-id="8ecf2-1927">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1927">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="8ecf2-1928">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1928">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="8ecf2-1929">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1929">Az.Accounts</span></span>
- <span data-ttu-id="8ecf2-1930">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1930">Changed from Az.Profile</span></span>
- <span data-ttu-id="8ecf2-1931">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1931">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-1932">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1932">Az.ApiManagement</span></span>
- <span data-ttu-id="8ecf2-1933">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1933">Fixes for #7002</span></span>
- <span data-ttu-id="8ecf2-1934">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1934">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="8ecf2-1935">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1935">Az.Batch</span></span>
- <span data-ttu-id="8ecf2-1936">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1936">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="8ecf2-1937">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1937">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="8ecf2-1938">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1938">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="8ecf2-1939">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1939">Az.Billing</span></span>
- <span data-ttu-id="8ecf2-1940">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1940">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="8ecf2-1941">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1941">Az.CognitivServices</span></span>
- <span data-ttu-id="8ecf2-1942">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1942">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="8ecf2-1943">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1943">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8ecf2-1944">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1944">Az.ContainerInstance</span></span>
- <span data-ttu-id="8ecf2-1945">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1945">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="8ecf2-1946">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1946">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="8ecf2-1947">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1947">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-1948">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1948">Az.DataLakeStore</span></span>
- <span data-ttu-id="8ecf2-1949">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1949">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="8ecf2-1950">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1950">Az.Monitor</span></span>
- <span data-ttu-id="8ecf2-1951">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1951">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="8ecf2-1952">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1952">Az.KeyVault</span></span>
- <span data-ttu-id="8ecf2-1953">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1953">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="8ecf2-1954">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1954">Az.MachineLearning</span></span>
- <span data-ttu-id="8ecf2-1955">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1955">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="8ecf2-1956">Az.Media</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1956">Az.Media</span></span>
- <span data-ttu-id="8ecf2-1957">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1957">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8ecf2-1958">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1958">Az.Network</span></span>
<span data-ttu-id="8ecf2-1959">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1959">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="8ecf2-1960">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1960">New cmdlets added:</span></span>
        - <span data-ttu-id="8ecf2-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1961">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ecf2-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1962">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ecf2-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1963">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ecf2-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1964">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ecf2-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1965">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="8ecf2-1966">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1966">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="8ecf2-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1967">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="8ecf2-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1968">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="8ecf2-1969">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1969">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="8ecf2-1970">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1970">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="8ecf2-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1971">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8ecf2-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1972">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="8ecf2-1973">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1973">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="8ecf2-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1974">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="8ecf2-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1975">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="8ecf2-1976">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1976">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="8ecf2-1977">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1977">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8ecf2-1978">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1978">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="8ecf2-1979">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1979">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="8ecf2-1980">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1980">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="8ecf2-1981">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1981">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="8ecf2-1982">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1982">Az.OperationalInsights</span></span>
- <span data-ttu-id="8ecf2-1983">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1983">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="8ecf2-1984">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1984">Az.Profile</span></span>
- <span data-ttu-id="8ecf2-1985">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1985">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-1986">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1986">Az.RecoveryServices</span></span>
- <span data-ttu-id="8ecf2-1987">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="8ecf2-1988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1988">Az.Resources</span></span>
- <span data-ttu-id="8ecf2-1989">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1989">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-1990">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1990">Az.ServiceFabric</span></span>
- <span data-ttu-id="8ecf2-1991">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1991">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="8ecf2-1992">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1992">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="8ecf2-1993">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1993">Az.SIgnalR</span></span>
- <span data-ttu-id="8ecf2-1994">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1994">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="8ecf2-1995">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1995">Az.Sql</span></span>
- <span data-ttu-id="8ecf2-1996">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1996">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="8ecf2-1997">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1997">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="8ecf2-1998">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1998">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="8ecf2-1999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-1999">Az.Storage</span></span>
- <span data-ttu-id="8ecf2-2000">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2000">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8ecf2-2001">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2001">Az.Websites</span></span>
- <span data-ttu-id="8ecf2-2002">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2002">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="8ecf2-2003">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2003">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="8ecf2-2004">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2004">General</span></span>

* <span data-ttu-id="8ecf2-2005">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2005">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="8ecf2-2006">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2006">Az.Compute</span></span>

* <span data-ttu-id="8ecf2-2007">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2007">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-2008">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2008">Az.DataLakeStore</span></span>

* <span data-ttu-id="8ecf2-2009">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2009">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="8ecf2-2010">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2010">Az.FrontDoor</span></span>

* <span data-ttu-id="8ecf2-2011">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2011">Fixed some broken links</span></span>
    - <span data-ttu-id="8ecf2-2012">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2012">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="8ecf2-2013">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2013">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="8ecf2-2014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2014">Az.RecoveryServices</span></span>

* <span data-ttu-id="8ecf2-2015">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2015">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="8ecf2-2016">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2016">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="8ecf2-2017">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2017">Az.Resources</span></span>

* <span data-ttu-id="8ecf2-2018">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2018">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="8ecf2-2019">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2019">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="8ecf2-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2020">Az.Sql</span></span>

* <span data-ttu-id="8ecf2-2021">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2021">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="8ecf2-2022">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2022">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="8ecf2-2023">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2023">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="8ecf2-2024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2024">Az.Storage</span></span>

* <span data-ttu-id="8ecf2-2025">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2025">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="8ecf2-2026">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2026">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="8ecf2-2027">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2027">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8ecf2-2028">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2028">Support Static Website configuration</span></span>
    - <span data-ttu-id="8ecf2-2029">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2029">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="8ecf2-2030">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2030">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="8ecf2-2031">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2031">Az.Websites</span></span>

* <span data-ttu-id="8ecf2-2032">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2032">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="8ecf2-2033">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2033">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="8ecf2-2034">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2034">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="8ecf2-2035">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2035">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="8ecf2-2036">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2036">Az.ApiManagement</span></span>
* <span data-ttu-id="8ecf2-2037">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2037">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="8ecf2-2038">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2038">Az.Automation</span></span>
* <span data-ttu-id="8ecf2-2039">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2039">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="8ecf2-2040">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2040">Added Update Management cmdlets</span></span>
* <span data-ttu-id="8ecf2-2041">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2041">Added Source Control cmdlets</span></span>
* <span data-ttu-id="8ecf2-2042">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2042">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="8ecf2-2043">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2043">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="8ecf2-2044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2044">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-2045">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2045">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="8ecf2-2046">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2046">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="8ecf2-2047">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2047">Az.ContainerInstance</span></span>
* <span data-ttu-id="8ecf2-2048">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2048">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="8ecf2-2049">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2049">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="8ecf2-2050">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2050">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="8ecf2-2051">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2051">Az.Network</span></span>
* <span data-ttu-id="8ecf2-2052">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2052">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="8ecf2-2053">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2053">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="8ecf2-2054">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2054">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="8ecf2-2055">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2055">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="8ecf2-2056">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2056">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8ecf2-2057">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2057">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="8ecf2-2058">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2058">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="8ecf2-2059">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2059">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8ecf2-2060">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2060">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="8ecf2-2061">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2061">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="8ecf2-2062">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2062">Az.Relay</span></span>
* <span data-ttu-id="8ecf2-2063">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2063">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="8ecf2-2064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2064">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-2065">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2065">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="8ecf2-2066">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2066">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="8ecf2-2067">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2067">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-2068">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2068">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-2069">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2069">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="8ecf2-2070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2070">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-2071">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2071">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="8ecf2-2072">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2072">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ecf2-2073">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2073">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ecf2-2074">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2074">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ecf2-2075">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2075">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="8ecf2-2076">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2076">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ecf2-2077">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2077">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ecf2-2078">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2078">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="8ecf2-2079">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2079">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="8ecf2-2080">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2080">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="8ecf2-2081">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2081">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="8ecf2-2082">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2082">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="8ecf2-2083">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2083">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8ecf2-2084">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2084">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="8ecf2-2085">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2085">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="8ecf2-2086">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2086">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="8ecf2-2087">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2087">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="8ecf2-2088">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2088">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8ecf2-2089">Generale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2089">General</span></span>
* <span data-ttu-id="8ecf2-2090">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2090">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="8ecf2-2091">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2091">Az.Profile</span></span>
* <span data-ttu-id="8ecf2-2092">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2092">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="8ecf2-2093">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2093">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="8ecf2-2094">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2094">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="8ecf2-2095">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2095">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="8ecf2-2096">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2096">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="8ecf2-2097">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2097">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="8ecf2-2098">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2098">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-2099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2099">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-2100">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2100">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2101">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-2102">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2102">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="8ecf2-2103">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2103">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="8ecf2-2104">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2104">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-2106">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2106">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="8ecf2-2107">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2107">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="8ecf2-2108">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2108">Az.Insights</span></span>
* <span data-ttu-id="8ecf2-2109">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2109">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="8ecf2-2110">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2110">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="8ecf2-2111">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2111">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="8ecf2-2112">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2112">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-2113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2113">Az.Network</span></span>
* <span data-ttu-id="8ecf2-2114">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2114">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="8ecf2-2115">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2115">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="8ecf2-2116">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2116">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="8ecf2-2117">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2117">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="8ecf2-2118">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2118">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8ecf2-2119">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2119">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8ecf2-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2120">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="8ecf2-2121">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2121">Az.PolicyInsights</span></span>
* <span data-ttu-id="8ecf2-2122">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2122">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-2123">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2123">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-2124">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2124">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="8ecf2-2125">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2125">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="8ecf2-2126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2126">Az.ServiceBus</span></span>
* <span data-ttu-id="8ecf2-2127">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2127">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="8ecf2-2128">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2128">Az.ServiceFabric</span></span>
* <span data-ttu-id="8ecf2-2129">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2129">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="8ecf2-2130">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2130">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="8ecf2-2131">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2131">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="8ecf2-2132">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2132">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="8ecf2-2133">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2133">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="8ecf2-2134">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2134">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="8ecf2-2135">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2135">Az.Profile</span></span>
* <span data-ttu-id="8ecf2-2136">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2136">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="8ecf2-2137">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2137">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-2138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2138">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-2139">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2139">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="8ecf2-2140">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2140">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="8ecf2-2141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2141">Az.DataLakeStore</span></span>
* <span data-ttu-id="8ecf2-2142">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2142">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8ecf2-2143">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2143">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8ecf2-2144">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2144">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8ecf2-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2145">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8ecf2-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2146">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-2147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2147">Az.Network</span></span>
* <span data-ttu-id="8ecf2-2148">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2148">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8ecf2-2149">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2149">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2150">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-2151">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2151">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8ecf2-2152">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2152">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="8ecf2-2153">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2153">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8ecf2-2154">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2154">Azure.Storage</span></span>
* <span data-ttu-id="8ecf2-2155">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2155">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8ecf2-2156">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2156">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8ecf2-2157">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2157">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="8ecf2-2158">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2158">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8ecf2-2159">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2159">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="8ecf2-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="8ecf2-2161">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2161">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="8ecf2-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2162">Az.Compute</span></span>
* <span data-ttu-id="8ecf2-2163">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2163">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8ecf2-2164">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2164">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="8ecf2-2165">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2165">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="8ecf2-2166">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2166">Az.DataFactoryV2</span></span>
* <span data-ttu-id="8ecf2-2167">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2167">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="8ecf2-2168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2168">Az.Network</span></span>
* <span data-ttu-id="8ecf2-2169">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2169">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8ecf2-2170">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2170">new cmdlets added</span></span>
    - <span data-ttu-id="8ecf2-2171">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2171">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ecf2-2172">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2172">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ecf2-2173">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2173">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ecf2-2174">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2174">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="8ecf2-2175">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2175">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="8ecf2-2176">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2176">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8ecf2-2177">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2177">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8ecf2-2178">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2178">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="8ecf2-2179">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2179">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="8ecf2-2180">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2180">Az.RedisCache</span></span>
* <span data-ttu-id="8ecf2-2181">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2181">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8ecf2-2182">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2182">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="8ecf2-2183">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2183">Az.Resources</span></span>
* <span data-ttu-id="8ecf2-2184">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2184">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="8ecf2-2185">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2185">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="8ecf2-2186">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2186">Az.Sql</span></span>
* <span data-ttu-id="8ecf2-2187">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2187">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="8ecf2-2188">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2188">Az.Websites</span></span>
* <span data-ttu-id="8ecf2-2189">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2189">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8ecf2-2190">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2190">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="8ecf2-2191">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2191">0.2.0 - September 2018</span></span>
 <span data-ttu-id="8ecf2-2192">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="8ecf2-2192">Initial Release</span></span>
