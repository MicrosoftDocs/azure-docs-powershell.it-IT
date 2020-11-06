---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: ed52eb21cfa5d192e4d7d0d79a2dc0847a5fd3ee
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490045"
---
# Modulo AzureRM. HDInsight
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per Microsoft Azure HDInsight nel Framework ARM (Azure Resource Manager). Questi cmdlet vengono usati per gestire i cluster HDInsight e i processi eseguiti su di essi. I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. HDInsight.

## Cmdlet AzureRM. HDInsight
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Aggiunge un'identità cluster a un oggetto di configurazione cluster.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Aggiunge una versione per un servizio in esecuzione in un cluster a un oggetto di configurazione cluster.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Aggiunge una personalizzazione del valore di configurazione Hadoop e/o una personalizzazione della raccolta condivisa hive a un oggetto di configurazione cluster.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Aggiunge un database SQL per fungere da Metastore hive o oozie a un oggetto di configurazione cluster.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Aggiunge un'azione di script a un oggetto di configurazione del cluster.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Aggiunge un oggetto di configurazione del cluster di sicurezza.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Aggiunge una chiave di archiviazione di Azure a un oggetto di configurazione cluster.

### [Disable-AzureRmHDInsightOperationsManagementSuite](Disable-AzureRmHDInsightOperationsManagementSuite.md)
Disabilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti interrompono il flusso nell'area di lavoro OMS specificata durante l'abilitazione.

### [Enable-AzureRmHDInsightOperationsManagementSuite](Enable-AzureRmHDInsightOperationsManagementSuite.md)
Abilita Operations Management Suite (OMS) in un cluster HDInsight e i registri rilevanti verranno inviati all'area di lavoro OMS specificata durante l'abilitazione.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Ottiene ed elenca tutti i cluster di Azure HDInsight associati all'abbonamento corrente o a un gruppo di risorse specificato oppure recupera un cluster specifico.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Ottiene l'elenco dei processi da un cluster e li elenca in ordine cronologico inverso o recupera un processo specifico.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Ottiene l'output del log per un processo dall'account di archiviazione associato a un cluster specificato.

### [Get-AzureRmHDInsightOperationsManagementSuite](Get-AzureRmHDInsightOperationsManagementSuite.md)
Ottiene lo stato dell'installazione di Operations Management Suite (OMS) nel cluster.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Ottiene le azioni di script permanenti per un cluster e le elenca in ordine cronologico oppure restituisce i dettagli per un'azione di script persistente specificata.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Ottiene le proprietà relative al servizio HDInsight, ad esempio posizioni e capacità disponibili.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Ottiene la cronologia delle azioni di script per un cluster e la elenca in ordine cronologico inverso o ottiene i dettagli di un'azione di script eseguita in precedenza.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Concede l'accesso HTTP al cluster.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Concede l'accesso RDP al cluster Windows.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Invia una query hive a un cluster HDInsight e recupera i risultati della query in un'unica operazione.

### [New-AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Crea un cluster di Azure HDInsight nel gruppo di risorse specificato per l'abbonamento corrente.

### [New-AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.

### [New-AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Crea un oggetto processo hive.

### [New-AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Crea un oggetto processo MapReduce.

### [New-AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Crea un oggetto processo Pig.

### [New-AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Crea un oggetto processo Sqoop.

### [New-AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Crea un oggetto processo di flusso MapReduce.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Rimuove il cluster HDInsight specificato dall'abbonamento corrente.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Rimuove un'azione di script persistente da un cluster HDInsight.

### [Revoke-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Disabilita l'accesso HTTP al cluster.

### [Revoke-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Disabilita l'accesso RDP a un cluster Windows.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Imposta il numero di nodi di lavoro in un cluster specificato.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Imposta l'impostazione predefinita dell'account di archiviazione in un oggetto di configurazione cluster.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Imposta un'azione di script eseguita in precedenza come azione di script persistente.

### [Start-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Avvia un processo di Azure HDInsight definito in un cluster specificato.

### [Stop-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Interrompe un processo in uso specificato in un cluster.

### [Invia-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Invia una nuova azione di script a un cluster di Azure HDInsight.

### [Usare-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Seleziona un cluster da usare con il cmdlet Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Attende il completamento o l'errore di un processo specificato.

