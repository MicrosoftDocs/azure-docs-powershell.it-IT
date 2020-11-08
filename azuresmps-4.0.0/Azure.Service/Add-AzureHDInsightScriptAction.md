---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023678"
---
# Add-AzureHDInsightScriptAction

## Sinossi
Aggiunge un'azione di script HDInsight.

## SINTASSI

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Questa versione di Azure PowerShell HDInsight è deprecata.
Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.
Usare la versione più recente di Azure PowerShell HDInsight.

Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Il cmdlet **Add-AzureHDInsightScriptAction** fornisce le funzionalità di Azure HDInsight usate per installare software aggiuntivo o per modificare la configurazione delle applicazioni eseguite in un cluster di Hadoop usando gli script di Windows PowerShell.

Un'azione di script viene eseguita sui nodi del cluster quando vengono distribuiti i cluster di HDInsight e vengono eseguiti dopo i nodi della configurazione completa di HDInsight del cluster.
L'azione script viene eseguita in privilegi di amministratore di sistema e fornisce i diritti di accesso completo ai nodi del cluster.
Puoi specificare ogni cluster con un elenco di azioni di script da eseguire in una sequenza specificata.

## ESEMPI

### Esempio 1: aggiungere un'azione di script a un cluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Il primo comando usa il cmdlet **New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight e quindi lo archivia nella variabile $config.

Il secondo comando usa il cmdlet **Add-AzureHDInsightScriptAction** per aggiungere l'azione script denominata TestScriptAction a $config.

Il comando finale usa il cmdlet **New-AzureHDInsightCluster** per creare un nuovo cluster di HDInsight che esegue l'azione di script archiviata in $config.

### Esempio 2: aggiungere più azioni di script a un cluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Il primo comando usa il cmdlet **New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight e quindi lo archivia nella variabile $config.

Il secondo comando usa il cmdlet **Add-AzureHDInsightScriptAction** per aggiungere l'azione di script specificata a $config e quindi usa l'operatore pipeline per passare una seconda volta $config a **Add-AzureHDInsightScriptAction** per aggiungere una seconda azione di script a $config.

Il comando finale usa il cmdlet **New-AzureHDInsightCluster** per creare un cluster che esegue le azioni di script in $config.

## PARAMETRI

### -ClusterRoleCollection
Specifica i nodi per cui eseguire uno script.
I valori accettabili per questo parametro sono: HeadNode o dataNode.

Puoi specificare un valore o entrambi i valori.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Specifica un oggetto Configuration.
Questo cmdlet aggiunge informazioni sulle azioni di script all'oggetto specificato da questo parametro.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Specifica il nome di un'azione di script.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameters
Specifica i parametri necessari per un'azione di script.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Specifica la posizione URI di uno script da eseguire.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


