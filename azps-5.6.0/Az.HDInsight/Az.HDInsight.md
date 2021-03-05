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
# Modulo Az.HDInsight
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di Azure PowerShell per Microsoft Azure HDInsight nel framework di Gestione risorse di Azure (ARM). Questi cmdlet vengono usati per gestire i cluster HDInsight e i processi che vengono eseguiti su di essi. I cmdlet sono presenti nello spazio dei nomi Microsoft.Azure.Commands.HDInsight.

## Cmdlet Az.HDInsight
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Aggiunge un'identità del cluster a un oggetto configurazione cluster.

### [Add-AzHDInsightVersion](Add-AzHDInsightComponentVersion.md)
Aggiunge una versione per un servizio in esecuzione in un cluster a un oggetto configurazione cluster.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa Hive a un oggetto configurazione cluster.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Aggiunge un SQL dati da fungere da hive o metastore Oozie a un oggetto configurazione cluster.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Aggiunge un'azione script a un oggetto configurazione cluster.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Aggiunge un profilo di sicurezza a un oggetto configurazione cluster.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Aggiunge una chiave di archiviazione di Azure a un oggetto di configurazione del cluster.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Disabilita il monitoraggio in un cluster HDInsight e il flusso dei log pertinenti nell'area di lavoro di monitoraggio specificata durante l'abilitazione non verrà più attivato.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Consente il monitoraggio in un cluster HDInsight e i log pertinenti verranno inviati all'area di lavoro di monitoraggio specificata durante l'abilitazione.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Ottiene ed elenca tutti i cluster Azure HDInsight associati alla sottoscrizione corrente o a un gruppo di risorse specificato oppure recupera uno specifico cluster.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Ottiene la configurazione della scala automatica del cluster HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Elenca gli host del cluster HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Recupera l'elenco di processi da un cluster ed elenca i processi in ordine cronologico inverso oppure recupera un processo specifico.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster specificato.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Ottiene lo stato di monitoraggio dell'installazione nel cluster.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Recupera le azioni degli script persistenti per un cluster ed elencale in ordine cronologico oppure recupera i dettagli per un'azione di script persistente specificata.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Ottiene le proprietà relative al servizio HDInsight, ad esempio le posizioni disponibili e la capacità.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Recupera la cronologia delle azioni dello script per un cluster e la elenca in ordine cronologico inverso oppure recupera i dettagli di un'azione di script eseguita in precedenza.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Invia una query Hive a un cluster HDInsight e recupera i risultati della query in un'unica operazione.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Crea un cluster HdInsight di Azure nel gruppo di risorse specificato per la sottoscrizione corrente.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Crea un oggetto non permanente che descrive la configurazione di gradazione automatica di un cluster HDInsight di Azure.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Crea una condizione di gradazioni automatica basata su pianificazione.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Crea un oggetto processo Hive.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Crea un oggetto processo MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Crea un oggetto processo sui maiali.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Crea un oggetto processo Dispo.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Crea un oggetto processo MapReduce di flusso.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Rimuove il cluster HDInsight specificato dalla sottoscrizione corrente.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Rimuove la configurazione di scala automatica del cluster HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Rimuove un'azione di script persistente da un cluster HDInsight.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Riavvia gli host specifici del cluster HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Imposta la configurazione della scala automatica di un cluster HDInsight di Azure.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Ruota la chiave di crittografia del disco del cluster HDInsight specificato.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Imposta il numero di nodi di lavoro in un cluster specificato.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Imposta l'impostazione predefinita dell'account di archiviazione in un oggetto configurazione cluster.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Imposta le credenziali HTTP del gateway di un cluster HdInsight di Azure.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Imposta un'azione script eseguita in precedenza come azione di script persistente.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Avvia un processo definito di Azure HDInsight in un cluster specificato.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Interrompe un processo in esecuzione specificato in un cluster.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Invia una nuova azione di script in un cluster HDInsight di Azure.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob cluster.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Attende il completamento o l'errore di un processo specificato.

