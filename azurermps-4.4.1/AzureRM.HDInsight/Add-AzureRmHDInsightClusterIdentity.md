---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: fc992b427e0c07b1f9db634f9369c21917ec9556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688640"
---
# Add-AzureRmHDInsightClusterIdentity

## Sinossi
Aggiunge un'identità cluster a un oggetto di configurazione cluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### CertificateFilePath (impostazione predefinita)
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CertificateFileContents
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmHDInsightClusterIdentity** aggiunge un'identità cluster all'oggetto di configurazione di Azure HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.

## ESEMPI

### Esempio 1: aggiungere informazioni sull'identità del cluster all'oggetto di configurazione del cluster
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

Questo comando aggiunge le informazioni sull'identità del cluster al cluster denominato your-Hadoop-001, consentendo al cluster di accedere a Azure Data Lake Store.

## PARAMETRI

### -AadTenantId
Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFileContents
Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFilePath
Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.
Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.
Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.
Questo oggetto viene creato dal cmdlet New-AzureRmHDInsightClusterConfig.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.
Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### AzureHDInsightConfig
Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline

### GUID
Il parametro "ObjectId" accetta il valore di tipo "GUID" dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmHDInsightClusterConfig](./New-AzureRmHDInsightClusterConfig.md)


