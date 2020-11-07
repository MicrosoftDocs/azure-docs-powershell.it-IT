---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 33e1e9ac0b62d378954280d8dd81361c0d075a1e
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/15/2019
ms.locfileid: "93673492"
---
# Modulo AZ. HDInsight
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per Microsoft Azure HDInsight nel Framework ARM (Azure Resource Manager). Questi cmdlet vengono usati per gestire i cluster HDInsight e i processi eseguiti su di essi. I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. HDInsight.

## Cmdlet AZ. HDInsight
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Aggiunge un'identità cluster a un oggetto di configurazione cluster.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Aggiunge una versione per un servizio in esecuzione in un cluster a un oggetto di configurazione cluster.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa hive a un oggetto di configurazione cluster.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Aggiunge un database SQL per fungere da Metastore hive o oozie a un oggetto di configurazione cluster.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Aggiunge un'azione di script a un oggetto di configurazione del cluster.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Aggiunge un profilo di sicurezza a un oggetto di configurazione cluster.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Aggiunge una chiave di archiviazione di Azure a un oggetto di configurazione cluster.

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
Disabilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro OMS specificata durante l'abilitazione.

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
Abilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro OMS specificata durante l'abilitazione.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Ottiene ed elenca tutti i cluster di Azure HDInsight associati all'abbonamento corrente o a un gruppo di risorse specificato oppure recupera un cluster specifico.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Ottiene l'elenco dei processi da un cluster e li elenca in ordine cronologico inverso o recupera un processo specifico.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster specificato.

### [Get-AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
Ottiene lo stato dell'installazione di Operations Management Suite (OMS) nel cluster.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Ottiene le azioni di script permanenti per un cluster e le elenca in ordine cronologico oppure restituisce i dettagli per un'azione di script persistente specificata.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Ottiene le proprietà relative al servizio HDInsight, ad esempio posizioni e capacità disponibili.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Ottiene la cronologia delle azioni di script per un cluster e la elenca in ordine cronologico inverso o ottiene i dettagli di un'azione di script eseguita in precedenza.

### [Grant-AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
Concede l'accesso RDP al cluster Windows.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Invia una query hive a un cluster HDInsight e recupera i risultati della query in un'unica operazione.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Crea un cluster di Azure HDInsight nel gruppo di risorse specificato per l'abbonamento corrente.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Crea un oggetto processo hive.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Crea un oggetto processo MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Crea un oggetto processo Pig.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Crea un oggetto processo Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Crea un oggetto processo di flusso MapReduce.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Rimuove il cluster HDInsight specificato dall'abbonamento corrente.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Rimuove un'azione di script persistente da un cluster HDInsight.

### [Revoke-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
Disabilita l'accesso RDP a un cluster Windows.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Imposta il numero di nodi di lavoro in un cluster specificato.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Imposta l'impostazione predefinita dell'account di archiviazione in un oggetto di configurazione cluster.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Imposta le credenziali HTTP del gateway di un cluster di Azure HDInsight.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Imposta un'azione di script eseguita in precedenza come azione di script persistente.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Avvia un processo di Azure HDInsight definito in un cluster specificato.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Interrompe un processo in uso specificato in un cluster.

### [Invia-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Invia una nuova azione di script a un cluster di Azure HDInsight.

### [Usare-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Attende il completamento o l'errore di un processo specificato.

