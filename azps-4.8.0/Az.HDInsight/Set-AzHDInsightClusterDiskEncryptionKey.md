---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191344"
---
# Set-AzHDInsightClusterDiskEncryptionKey

## Sinossi
Ruota la chiave di crittografia del disco del cluster HDInsight specificato.

## SINTASSI

### SetByNameParameterSet (impostazione predefinita)
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceIdParameterSet
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByInputObjectParameterSet
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Ruotare la chiave di crittografia del disco del cluster HDInsight specificato. Per questa operazione, il cluster deve avere accesso sia alla chiave corrente che alla nuova chiave prevista, in caso contrario l'operazione di rotazione dei tasti non riuscirà.

## ESEMPI

### Esempio 1
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### Esempio 2
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyName
Ottiene o imposta il nome della chiave di crittografia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyVersion
Ottiene o imposta la versione della chiave di crittografia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionVaultUri
Ottiene o imposta l'URI del Vault di crittografia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Ottiene o imposta l'oggetto di input.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Ottiene o imposta il nome del cluster.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ottiene o imposta il nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Ottiene o imposta l'ID risorsa.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Management. HDInsight. Models. cluster

## Note

## COLLEGAMENTI CORRELATI

[Crittografia del disco di chiave gestita dal cliente](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
