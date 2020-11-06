---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507931"
---
# Start-AzureRmSiteRecoveryUnplannedFailoverJob

## Sinossi
Avvia il failover non pianificato per un'entità di protezione del ripristino del sito o un piano di ripristino.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByPEObject (impostazione predefinita)
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPIObject
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureRmSiteRecoveryUnplannedFailoverJob** avvia il failover non pianificato di un'entità o un piano di ripristino di un sito di ripristino di Azure.
Puoi verificare se il processo viene eseguito correttamente usando il cmdlet Get-AzureRmSiteRecoveryJob.

## ESEMPI

## PARAMETRI

### -DataEncryptionPrimaryCertFile
Specifica il file di certificato principale.

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

### -DataEncryptionSecondaryCertFile
Specifica il file di certificato secondario.

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

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Direzione
Specifica la direzione del failover.
I valori accettabili per questo parametro sono i seguenti:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PerformSourceSideActions
Indica che l'azione può eseguire operazioni del sito di origine.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
Specifica l'oggetto entità di protezione del ripristino del sito.

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPlan
Specifica un oggetto piano di ripristino.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### ASRProtectionEntity
Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline

### ASRRecoveryPlan
Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline

### ASRReplicationProtectedItem
Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmSiteRecoveryJob](./Get-AzureRmSiteRecoveryJob.md)


