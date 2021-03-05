---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: ec924f7424d2b522e6bbd9ce1db51e8c920ec663
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990133"
---
# <span data-ttu-id="ff105-101">Modulo Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff105-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="ff105-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff105-102">Description</span></span>
<span data-ttu-id="ff105-103">Gli argomenti di questa sezione documentano i cmdlet di Azure PowerShell per Microsoft Azure HDInsight nel framework di Gestione risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="ff105-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="ff105-104">Questi cmdlet vengono usati per gestire i cluster HDInsight e i processi che vengono eseguiti su di essi.</span><span class="sxs-lookup"><span data-stu-id="ff105-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="ff105-105">I cmdlet sono presenti nello spazio dei nomi Microsoft.Azure.Commands.HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="ff105-106">Cmdlet Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff105-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="ff105-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="ff105-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="ff105-108">Aggiunge un'identità del cluster a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-109">Add-AzHDInsightVersion</span><span class="sxs-lookup"><span data-stu-id="ff105-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="ff105-110">Aggiunge una versione per un servizio in esecuzione in un cluster a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="ff105-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="ff105-112">Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa Hive a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="ff105-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="ff105-114">Aggiunge un SQL dati da fungere da hive o metastore Oozie a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="ff105-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="ff105-116">Aggiunge un'azione script a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ff105-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="ff105-118">Aggiunge un profilo di sicurezza a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ff105-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="ff105-120">Aggiunge una chiave di archiviazione di Azure a un oggetto di configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ff105-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="ff105-122">Disabilita il monitoraggio in un cluster HDInsight e il flusso dei log pertinenti nell'area di lavoro di monitoraggio specificata durante l'abilitazione non verrà più attivato.</span><span class="sxs-lookup"><span data-stu-id="ff105-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="ff105-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ff105-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="ff105-124">Consente il monitoraggio in un cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio specificata durante l'abilitazione.</span><span class="sxs-lookup"><span data-stu-id="ff105-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="ff105-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ff105-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="ff105-126">Ottiene ed elenca tutti i cluster Azure HDInsight associati alla sottoscrizione corrente o a un gruppo di risorse specificato oppure recupera uno specifico cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="ff105-127">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff105-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="ff105-128">Ottiene la configurazione della scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-129">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="ff105-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="ff105-130">Elenca gli host del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ff105-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="ff105-132">Recupera l'elenco di processi da un cluster ed elenca i processi in ordine cronologico inverso oppure recupera un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="ff105-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="ff105-133">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="ff105-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="ff105-134">Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="ff105-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="ff105-135">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ff105-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="ff105-136">Ottiene lo stato di monitoraggio dell'installazione nel cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="ff105-137">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ff105-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="ff105-138">Recupera le azioni degli script persistenti per un cluster ed elencale in ordine cronologico oppure recupera i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="ff105-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="ff105-139">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="ff105-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="ff105-140">Ottiene le proprietà relative al servizio HDInsight, ad esempio le posizioni disponibili e la capacità.</span><span class="sxs-lookup"><span data-stu-id="ff105-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="ff105-141">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="ff105-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="ff105-142">Recupera la cronologia delle azioni dello script per un cluster e la elenca in ordine cronologico inverso oppure recupera i dettagli di un'azione di script eseguita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="ff105-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="ff105-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="ff105-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="ff105-144">Invia una query Hive a un cluster HDInsight e recupera i risultati della query in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="ff105-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="ff105-145">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ff105-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="ff105-146">Crea un cluster HdInsight di Azure nel gruppo di risorse specificato per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ff105-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="ff105-147">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff105-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="ff105-148">Crea un oggetto non permanente che descrive la configurazione di gradazione automatica di un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff105-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="ff105-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="ff105-150">Crea una condizione di gradazioni automatica basata su pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ff105-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="ff105-151">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ff105-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="ff105-152">Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="ff105-153">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ff105-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="ff105-154">Crea un oggetto processo Hive.</span><span class="sxs-lookup"><span data-stu-id="ff105-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="ff105-155">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ff105-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="ff105-156">Crea un oggetto processo MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ff105-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="ff105-157">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ff105-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="ff105-158">Crea un oggetto processo sui maiali.</span><span class="sxs-lookup"><span data-stu-id="ff105-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="ff105-159">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ff105-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="ff105-160">Crea un oggetto processo Dispo.</span><span class="sxs-lookup"><span data-stu-id="ff105-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="ff105-161">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ff105-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="ff105-162">Crea un oggetto processo MapReduce di flusso.</span><span class="sxs-lookup"><span data-stu-id="ff105-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="ff105-163">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ff105-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="ff105-164">Rimuove il cluster HDInsight specificato dalla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ff105-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="ff105-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff105-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="ff105-166">Rimuove la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-167">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ff105-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="ff105-168">Rimuove un'azione di script persistente da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-169">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="ff105-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="ff105-170">Riavvia gli host specifici del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ff105-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff105-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="ff105-172">Imposta la configurazione della scala automatica di un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff105-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-173">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ff105-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="ff105-174">Ruota la chiave di crittografia del disco del cluster HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="ff105-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="ff105-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="ff105-176">Imposta il numero di nodi di lavoro in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="ff105-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="ff105-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ff105-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="ff105-178">Imposta l'impostazione predefinita dell'account di archiviazione in un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="ff105-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="ff105-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="ff105-180">Imposta le credenziali HTTP del gateway di un cluster HdInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff105-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ff105-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="ff105-182">Imposta un'azione script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="ff105-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="ff105-183">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ff105-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="ff105-184">Avvia un processo definito di Azure HDInsight in un cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="ff105-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="ff105-185">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ff105-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="ff105-186">Interrompe un processo in esecuzione specificato in un cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="ff105-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="ff105-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="ff105-188">Invia una nuova azione di script in un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff105-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="ff105-189">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ff105-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="ff105-190">Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob cluster.</span><span class="sxs-lookup"><span data-stu-id="ff105-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="ff105-191">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ff105-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="ff105-192">Attende il completamento o l'errore di un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="ff105-192">Waits for the completion or failure of a specified job.</span></span>

