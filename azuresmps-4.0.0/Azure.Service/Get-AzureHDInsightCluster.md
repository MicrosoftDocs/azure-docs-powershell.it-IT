---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023602"
---
# Get-AzureHDInsightCluster

## Sinossi
Ottiene un cluster HDInsight.

## SINTASSI

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Questa versione di Azure PowerShell HDInsight è deprecata.
Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.
Usare la versione più recente di Azure PowerShell HDInsight.

Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Il cmdlet **Get-AzureHDInsightCluster** ottiene i cluster di servizi di Azure HDInsight per l'abbonamento corrente.
Puoi usare il parametro *Name* per ottenere un cluster specifico.

## ESEMPI

### Esempio 1: ottenere i cluster in un abbonamento
```
PS C:\> Get-AzureHDInsightCluster
```

Questo comando consente di ottenere informazioni sui cluster HDInsight nell'abbonamento corrente.

## PARAMETRI

### -Certificato
Specifica il certificato di gestione per un abbonamento a Azure.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Specifica l'endpoint da usare per la connessione a Azure.
Se non specifichi questo parametro, questo cmdlet usa l'endpoint predefinito.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Specifica lo spazio dei nomi di un servizio HDInsight.
Se non specifichi questo parametro, questo cmdlet usa lo spazio dei nomi predefinito.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Indica se gli errori SSL (Secure Sockets Layer) vengono ignorati.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome di un cluster HDInsight da ottenere.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Sottoscrizione
Specifica l'abbonamento che contiene il cluster HDInsight per ottenere.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
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

[Remove-AzureHDInsightCluster](./Remove-AzureHDInsightCluster.md)

[Usare-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


